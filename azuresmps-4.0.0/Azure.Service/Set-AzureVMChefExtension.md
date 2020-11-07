---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 021D4624-AE78-4FBE-B1DE-A8A84DF1FC90
online version: ''
schema: 2.0.0
ms.openlocfilehash: 52c3a26887e42884025234ba5f1a7330c258e903
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946045"
---
# <span data-ttu-id="89636-101">Set-AzureVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="89636-101">Set-AzureVMChefExtension</span></span>

## <span data-ttu-id="89636-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="89636-102">SYNOPSIS</span></span>
<span data-ttu-id="89636-103">Adiciona a extensão chefe à máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="89636-103">Adds the Chef extension to the virtual machine.</span></span>

## <span data-ttu-id="89636-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="89636-104">SYNTAX</span></span>

### <span data-ttu-id="89636-105">Windows (padrão)</span><span class="sxs-lookup"><span data-stu-id="89636-105">Windows (Default)</span></span>
```
Set-AzureVMChefExtension [-Version <String>] -ValidationPem <String> [-ClientRb <String>]
 [-BootstrapOptions <String>] [-RunList <String>] [-JsonAttribute <String>] [-ChefDaemonInterval <String>]
 [-ChefServerUrl <String>] [-ValidationClientName <String>] [-OrganizationName <String>]
 [-BootstrapVersion <String>] [-Daemon <String>] [-Secret <String>] [-SecretFile <String>] [-Windows]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="89636-106">Linux</span><span class="sxs-lookup"><span data-stu-id="89636-106">Linux</span></span>
```
Set-AzureVMChefExtension [-Version <String>] -ValidationPem <String> [-ClientRb <String>]
 [-BootstrapOptions <String>] [-RunList <String>] [-JsonAttribute <String>] [-ChefDaemonInterval <String>]
 [-ChefServerUrl <String>] [-ValidationClientName <String>] [-OrganizationName <String>]
 [-BootstrapVersion <String>] [-Daemon <String>] [-Secret <String>] [-SecretFile <String>] [-Linux]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="89636-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="89636-107">DESCRIPTION</span></span>
<span data-ttu-id="89636-108">O cmdlet **set-AzureVMChefExtension** adiciona a extensão chefe à máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="89636-108">The **Set-AzureVMChefExtension** cmdlet adds the Chef extension to the virtual machine.</span></span>

## <span data-ttu-id="89636-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="89636-109">EXAMPLES</span></span>

### <span data-ttu-id="89636-110">Exemplo 1: adicionar uma extensão chefe a um computador virtual do Windows</span><span class="sxs-lookup"><span data-stu-id="89636-110">Example 1: Add a Chef extension to a Windows virtual machine</span></span>
```
PS C:\> Set-AzureVMChefExtension -VM $VM -ValidationPem "C:\\myorg-validator.pem" -ClientRb "C:\\client.rb" -RunList "Apache" -Windows;
```

<span data-ttu-id="89636-111">Esse comando adiciona uma extensão chefe a um computador virtual do Windows.</span><span class="sxs-lookup"><span data-stu-id="89636-111">This command adds a Chef extension to a Windows virtual machine.</span></span>
<span data-ttu-id="89636-112">Quando a máquina virtual chega, ela é disparada com chefe e executa o Apache.</span><span class="sxs-lookup"><span data-stu-id="89636-112">When the virtual machine comes up, it is bootstrapped with Chef and runs Apache on it.</span></span>

### <span data-ttu-id="89636-113">Exemplo 2: adicionar uma extensão chefe a um computador virtual do Windows com inicialização</span><span class="sxs-lookup"><span data-stu-id="89636-113">Example 2: Add a Chef extension to a Windows virtual machine with bootstrapping</span></span>
```
PS C:\> Set-AzureVMChefExtension -VM $VM -ValidationPem "C:\\myorg-validator.pem" -BootstrapOptions '{"chef_node_name":"your_node_name","chef_server_url":"https://api.opscode.com/organizations/some-org", "validation_client_name":"some-org-validator"}' -RunList "Apache" -Windows;
```

<span data-ttu-id="89636-114">Esse comando adiciona a extensão chefe a um computador virtual do Windows.</span><span class="sxs-lookup"><span data-stu-id="89636-114">This command adds the Chef extension to a Windows virtual machine.</span></span>
<span data-ttu-id="89636-115">Quando a máquina virtual é iniciada, ela é iniciada com chefe e executa o Apache.</span><span class="sxs-lookup"><span data-stu-id="89636-115">When the virtual machine launches, it is bootstrapped with Chef and runs Apache on it.</span></span>
<span data-ttu-id="89636-116">Após a inicialização, a máquina virtual refere-se à *bootstrapoptions* especificada no formato JSON.</span><span class="sxs-lookup"><span data-stu-id="89636-116">After bootstrapping, the virtual machine refers to the *BootstrapOptions* specified in JSON format.</span></span>

### <span data-ttu-id="89636-117">Exemplo 3: adicionar uma extensão chefe a um computador virtual do Windows e instalar o Apache e o GIT</span><span class="sxs-lookup"><span data-stu-id="89636-117">Example 3: Add a Chef extension to a Windows virtual machine and install Apache and GIT</span></span>
```
PS C:\> Set-AzureVMChefExtension -VM $VM -ValidationPem "C:\\myorg-validator.pem" -ChefServerUrl "http://ipaddress:port" -ValidationClientName "MyOrg-Validator" -RunList "apache, git" -Windows;
```

<span data-ttu-id="89636-118">Esse comando adiciona a extensão chefe a um computador virtual do Windows.</span><span class="sxs-lookup"><span data-stu-id="89636-118">This command adds the Chef extension to a Windows virtual machine.</span></span>
<span data-ttu-id="89636-119">Quando a máquina virtual é iniciada, ela é iniciada com chefe e o Apache e o GIT são instalados.</span><span class="sxs-lookup"><span data-stu-id="89636-119">When the virtual machine launches, it is bootstrapped with Chef and have Apache and GIT installed.</span></span>
<span data-ttu-id="89636-120">Se você não fornecer o Client. rb, será necessário fornecer a URL e o nome do cliente de validação do servidor chefe.</span><span class="sxs-lookup"><span data-stu-id="89636-120">If you do not provide the client.rb, you need to provide the Chef server URL and validation client name.</span></span>

### <span data-ttu-id="89636-121">Exemplo 4: adicionar uma extensão chefe a um computador virtual Linux</span><span class="sxs-lookup"><span data-stu-id="89636-121">Example 4: Add a Chef extension to a Linux virtual machine</span></span>
```
PS C:\> Set-AzureVMChefExtension -VM $VM -ValidationPem "C:\\myorg-validator.pem" -ChefServerUrl "http://ipaddress:port" -OrganizationName "MyOrg" -Linux;
```

<span data-ttu-id="89636-122">Esse comando adiciona a extensão chefe a um computador virtual Linux.</span><span class="sxs-lookup"><span data-stu-id="89636-122">This command adds the Chef extension to a Linux virtual machine.</span></span>
<span data-ttu-id="89636-123">Quando a máquina virtual é iniciada, ela é iniciada com chefe.</span><span class="sxs-lookup"><span data-stu-id="89636-123">When the virtual machine launches, it is bootstrapped with Chef.</span></span>
<span data-ttu-id="89636-124">Se você não fornecer o Client. rb, será necessário fornecer a URL e a organização do servidor chefe.</span><span class="sxs-lookup"><span data-stu-id="89636-124">If you do not provide the client.rb, you need to provide the Chef server URL and organization.</span></span>

## <span data-ttu-id="89636-125">OS</span><span class="sxs-lookup"><span data-stu-id="89636-125">PARAMETERS</span></span>

### <span data-ttu-id="89636-126">-Bootstrapoptions</span><span class="sxs-lookup"><span data-stu-id="89636-126">-BootstrapOptions</span></span>
<span data-ttu-id="89636-127">Especifica as opções de inicialização no formato JSON (JavaScript Object Notation).</span><span class="sxs-lookup"><span data-stu-id="89636-127">Specifies bootstrap options in JavaScript Object Notation (JSON) format.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89636-128">-BootstrapVersion</span><span class="sxs-lookup"><span data-stu-id="89636-128">-BootstrapVersion</span></span>
<span data-ttu-id="89636-129">Especifica a versão do cliente chefe que é instalada juntamente com a extensão.</span><span class="sxs-lookup"><span data-stu-id="89636-129">Specifies the version of the Chef client that is installed together with the extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89636-130">-ChefDaemonInterval</span><span class="sxs-lookup"><span data-stu-id="89636-130">-ChefDaemonInterval</span></span>
<span data-ttu-id="89636-131">Especifica a frequência (em minutos) em que o chefe-serviço é executado.</span><span class="sxs-lookup"><span data-stu-id="89636-131">Specifies the frequency (in minutes) at which the chef-service runs.</span></span> <span data-ttu-id="89636-132">Se, caso não queira que o chefe-serviço seja instalado na máquina virtual do Azure, defina o valor como 0 nesse campo.</span><span class="sxs-lookup"><span data-stu-id="89636-132">If in case you don't want the chef-service to be installed on the Azure VM then set value as 0 in this field.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ChefServiceInterval

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89636-133">-ChefServerUrl</span><span class="sxs-lookup"><span data-stu-id="89636-133">-ChefServerUrl</span></span>
<span data-ttu-id="89636-134">Especifica a URL do servidor chefe.</span><span class="sxs-lookup"><span data-stu-id="89636-134">Specifies the URL of the Chef server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89636-135">-ClientRb</span><span class="sxs-lookup"><span data-stu-id="89636-135">-ClientRb</span></span>
<span data-ttu-id="89636-136">Especifica o caminho completo do chefe cliente. rb.</span><span class="sxs-lookup"><span data-stu-id="89636-136">Specifies the full path of the Chef client.rb.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89636-137">-Daemon</span><span class="sxs-lookup"><span data-stu-id="89636-137">-Daemon</span></span>
<span data-ttu-id="89636-138">Configura o serviço chefe-cliente para execução automática.</span><span class="sxs-lookup"><span data-stu-id="89636-138">Configures the chef-client service for unattended execution.</span></span> <span data-ttu-id="89636-139">A plataforma do nó deve ser Windows.</span><span class="sxs-lookup"><span data-stu-id="89636-139">The node platform should be Windows.</span></span>
<span data-ttu-id="89636-140">Opções permitidas: ' none ', ' Service ' e ' Task '.</span><span class="sxs-lookup"><span data-stu-id="89636-140">Allowed options: 'none','service' and 'task'.</span></span>
<span data-ttu-id="89636-141">None-atualmente impede que o serviço chefe-cliente seja configurado como um serviço.</span><span class="sxs-lookup"><span data-stu-id="89636-141">none - Currently prevents the chef-client service from being configured as a service.</span></span>
<span data-ttu-id="89636-142">serviço-configura o chefe-cliente para ser executado automaticamente em segundo plano como um serviço.</span><span class="sxs-lookup"><span data-stu-id="89636-142">service - Configures the chef-client to run automatically in the background as a service.</span></span>
<span data-ttu-id="89636-143">Task-configura o chefe-cliente para ser executado automaticamente em segundo plano como uma tarefa secheduled.</span><span class="sxs-lookup"><span data-stu-id="89636-143">task - Configures the chef-client to run automatically in the background as a secheduled task.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89636-144">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="89636-144">-InformationAction</span></span>
<span data-ttu-id="89636-145">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="89636-145">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="89636-146">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="89636-146">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="89636-147">Contínuo</span><span class="sxs-lookup"><span data-stu-id="89636-147">Continue</span></span>
- <span data-ttu-id="89636-148">Ignorar</span><span class="sxs-lookup"><span data-stu-id="89636-148">Ignore</span></span>
- <span data-ttu-id="89636-149">Inquire</span><span class="sxs-lookup"><span data-stu-id="89636-149">Inquire</span></span>
- <span data-ttu-id="89636-150">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="89636-150">SilentlyContinue</span></span>
- <span data-ttu-id="89636-151">Finaliza</span><span class="sxs-lookup"><span data-stu-id="89636-151">Stop</span></span>
- <span data-ttu-id="89636-152">Suspensão</span><span class="sxs-lookup"><span data-stu-id="89636-152">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89636-153">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="89636-153">-InformationVariable</span></span>
<span data-ttu-id="89636-154">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="89636-154">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89636-155">-Jsonattribute</span><span class="sxs-lookup"><span data-stu-id="89636-155">-JsonAttribute</span></span>
<span data-ttu-id="89636-156">Uma cadeia de caracteres JSON a ser adicionada à primeira execução do chefe-cliente.</span><span class="sxs-lookup"><span data-stu-id="89636-156">A JSON string to be added to the first run of chef-client.</span></span> <span data-ttu-id="89636-157">por exemplo:-Jsonattribute ' {"foo": "barra"} '</span><span class="sxs-lookup"><span data-stu-id="89636-157">e.g. -JsonAttribute '{"foo" : "bar"}'</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89636-158">-Linux</span><span class="sxs-lookup"><span data-stu-id="89636-158">-Linux</span></span>
<span data-ttu-id="89636-159">Indica que esse cmdlet cria uma máquina virtual baseada em Linux.</span><span class="sxs-lookup"><span data-stu-id="89636-159">Indicates that this cmdlet creates a Linux based virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89636-160">-OrganizationName</span><span class="sxs-lookup"><span data-stu-id="89636-160">-OrganizationName</span></span>
<span data-ttu-id="89636-161">Especifica o nome da organização da extensão chefe.</span><span class="sxs-lookup"><span data-stu-id="89636-161">Specifies the organization name of the Chef extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89636-162">-Perfil</span><span class="sxs-lookup"><span data-stu-id="89636-162">-Profile</span></span>
<span data-ttu-id="89636-163">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="89636-163">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="89636-164">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="89636-164">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89636-165">-RunList</span><span class="sxs-lookup"><span data-stu-id="89636-165">-RunList</span></span>
<span data-ttu-id="89636-166">Especifica a lista de execução do nó chefe.</span><span class="sxs-lookup"><span data-stu-id="89636-166">Specifies the Chef node run list.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89636-167">-Segredo</span><span class="sxs-lookup"><span data-stu-id="89636-167">-Secret</span></span>
<span data-ttu-id="89636-168">A chave de criptografia usada para criptografar e descriptografar os valores de item do conjunto de dados.</span><span class="sxs-lookup"><span data-stu-id="89636-168">The encryption key used to encrypt and decrypt the data bag item values.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89636-169">-Secretfile</span><span class="sxs-lookup"><span data-stu-id="89636-169">-SecretFile</span></span>
<span data-ttu-id="89636-170">O caminho para o arquivo que contém a chave de criptografia usada para criptografar e descriptografar os valores de item do conjunto de dados.</span><span class="sxs-lookup"><span data-stu-id="89636-170">The path to the file that contains the encryption key used to encrypt and decrypt the data bag item values.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89636-171">-ValidationClientName</span><span class="sxs-lookup"><span data-stu-id="89636-171">-ValidationClientName</span></span>
<span data-ttu-id="89636-172">Especifica o nome do cliente de validação.</span><span class="sxs-lookup"><span data-stu-id="89636-172">Specifies the name of the validation client.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89636-173">-ValidationPem</span><span class="sxs-lookup"><span data-stu-id="89636-173">-ValidationPem</span></span>
<span data-ttu-id="89636-174">Especifica o caminho do arquivo do chefe Validator. PEM.</span><span class="sxs-lookup"><span data-stu-id="89636-174">Specifies the Chef validator .pem file path.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89636-175">-Versão</span><span class="sxs-lookup"><span data-stu-id="89636-175">-Version</span></span>
<span data-ttu-id="89636-176">Especifica o número da versão da extensão chefe.</span><span class="sxs-lookup"><span data-stu-id="89636-176">Specifies the version number of the Chef extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89636-177">-VM</span><span class="sxs-lookup"><span data-stu-id="89636-177">-VM</span></span>
<span data-ttu-id="89636-178">Especifica o objeto da máquina virtual persistente.</span><span class="sxs-lookup"><span data-stu-id="89636-178">Specifies the persistent virtual machine object.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="89636-179">-Windows</span><span class="sxs-lookup"><span data-stu-id="89636-179">-Windows</span></span>
<span data-ttu-id="89636-180">Indica que esse cmdlet cria um computador virtual do Windows.</span><span class="sxs-lookup"><span data-stu-id="89636-180">Indicates that this cmdlet creates a Windows virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89636-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89636-181">CommonParameters</span></span>
<span data-ttu-id="89636-182">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89636-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89636-183">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89636-183">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89636-184">SENSORES</span><span class="sxs-lookup"><span data-stu-id="89636-184">INPUTS</span></span>

## <span data-ttu-id="89636-185">EXIBE</span><span class="sxs-lookup"><span data-stu-id="89636-185">OUTPUTS</span></span>

## <span data-ttu-id="89636-186">INFORMA</span><span class="sxs-lookup"><span data-stu-id="89636-186">NOTES</span></span>

## <span data-ttu-id="89636-187">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="89636-187">RELATED LINKS</span></span>

[<span data-ttu-id="89636-188">Get-AzureVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="89636-188">Get-AzureVMChefExtension</span></span>](./Get-AzureVMChefExtension.md)

[<span data-ttu-id="89636-189">Remove-AzureVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="89636-189">Remove-AzureVMChefExtension</span></span>](./Remove-AzureVMChefExtension.md)


