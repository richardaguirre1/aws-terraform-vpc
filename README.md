<h1>AWS VPC con Terraform</h1>

<p>Este repositorio contiene una implementación de infraestructura como código (IaC) utilizando Terraform para desplegar una red virtual (VPC) en AWS. Incluye la creación de subredes públicas y privadas, instancias EC2, tablas de rutas, un Internet Gateway y un VPC Endpoint.</p>

<h2>Características</h2>
<ul>
  <li>Creación de una VPC personalizada.</li>
  <li>Subred pública con su rango de IPs.</li>
  <li>Subred privada con su rango de IPs.</li>
  <li>Internet Gateway para acceso a Internet desde la subred pública.</li>
  <li>Instancia EC2 en la subred pública.</li>
  <li>Instancia EC2 en la subred privada.</li>
  <li>Tablas de rutas asociadas a cada subred.</li>
  <li>Configuración de un VPC Endpoint para servicios privados de AWS.</li>
</ul>

<h2>Estructura del Proyecto</h2>
<ul>
  <li><code>main.tf</code>: Define los recursos principales de la infraestructura.</li>
  <li><code>variables.tf</code>: Contiene las variables utilizadas en el proyecto.</li>
  <li><code>outputs.tf</code>: Especifica las salidas que proporciona Terraform después de la implementación.</li>
  <li><code>provider.tf</code>: Configura el proveedor de AWS para Terraform.</li>
  <li><code>remote_backend_s3.tf</code>: Configura el backend remoto en S3 para el estado de Terraform.</li>
  <li><code>terraform.tfvars</code>: Define los valores específicos para las variables.</li>
  <li>Directorios adicionales:
    <ul>
      <li><code>networking/</code>: Configuración de la red (VPC, subredes, etc.).</li>
      <li><code>ec2/</code>: Definición de las instancias EC2.</li>
      <li><code>security-groups/</code>: Configuración de los grupos de seguridad.</li>
      <li><code>vpc-endpoint/</code>: Configuración del VPC Endpoint.</li>
    </ul>
  </li>
</ul>

<h2>Prerrequisitos</h2>
<ul>
  <li>Tener una cuenta de AWS con las credenciales configuradas.</li>
  <li>Instalar <a href="https://www.terraform.io/downloads.html" target="_blank">Terraform</a> (versión 1.0 o superior).</li>
  <li>Configurar el archivo <code>terraform.tfvars</code> con los valores adecuados para tu entorno.</li>
</ul>

<h2>Uso</h2>
<ol>
  <li>Clona este repositorio:
    <pre><code>git clone https://github.com/richardaguirre1/aws-terraform-vpc.git
cd aws-terraform-vpc</code></pre>
  </li>
  <li>Inicializa Terraform:
    <pre><code>terraform init</code></pre>
  </li>
  <li>Revisa el plan de implementación:
    <pre><code>terraform plan</code></pre>
  </li>
  <li>Aplica la configuración para desplegar la infraestructura:
    <pre><code>terraform apply</code></pre>
  </li>
  <li>Para destruir la infraestructura creada:
    <pre><code>terraform destroy</code></pre>
  </li>
</ol>

<h2>Autor</h2>
<p><a href="https://github.com/richardaguirre1" target="_blank">Richard Devops</a></p>
