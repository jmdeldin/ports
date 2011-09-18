desc 'Add ports to the index'
task :index do |t|
  sh 'portindex -f -d'
end

desc 'Create a new portfile'
task :new, :category, :port do |t, args|
  path = File.join(args.category, '/', args.port)
  mkdir_p path
  chdir path

  header = <<-EOF.gsub(/^\s+/, '')
    # -*- coding: utf-8; mode: tcl; tab-width: 4; indent-tabs-mode: nil; c-basic-offset: 4 -*- vim:fenc=utf-8:ft=tcl:et:sw=4:ts=4:sts=4

    # $Id$

    PortSystem          1.0

    name                <port>
    version             version
    categories          <category>
    platforms           darwin
    maintainers         jmdeldin.com:macports
    description
    long_description
    homepage
    master_sites
    license
    distfiles
    checksums
  EOF

  header.gsub!(/<port>/, args.port)
  header.gsub!(/<category>/, args.category)

  unless File.exists?('Portfile')
    File.open('Portfile', 'w') { |f| f.puts(header) }
  end
end

