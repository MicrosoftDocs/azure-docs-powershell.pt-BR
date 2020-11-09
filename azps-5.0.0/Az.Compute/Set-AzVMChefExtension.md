---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: CC306D8C-A5EE-4655-B686-E5A77CCE5042
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmchefextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMChefExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMChefExtension.md
ms.openlocfilehash: 2821e9404fe4101415aa04a8b0d331b3066563df
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94280391"
---
# <span data-ttu-id="de0cd-101">Set-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="de0cd-101">Set-AzVMChefExtension</span></span>

## <span data-ttu-id="de0cd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="de0cd-102">SYNOPSIS</span></span>
<span data-ttu-id="de0cd-103">Adiciona uma extensão chefe a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="de0cd-103">Adds a Chef extension to a virtual machine.</span></span>

## <span data-ttu-id="de0cd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="de0cd-104">SYNTAX</span></span>

### <span data-ttu-id="de0cd-105">Linux</span><span class="sxs-lookup"><span data-stu-id="de0cd-105">Linux</span></span>
```
Set-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-TypeHandlerVersion] <String>]
 -ValidationPem <String> [-ClientRb <String>] [-BootstrapOptions <String>] [-JsonAttribute <String>]
 [-ChefDaemonInterval <String>] [-Daemon <String>] [-Secret <String>] [-SecretFile <String>]
 [-RunList <String>] [-ChefServerUrl <String>] [-ValidationClientName <String>] [-OrganizationName <String>]
 [-BootstrapVersion <String>] [-Linux] [[-Location] <String>] [[-Name] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de0cd-106">Windows</span><span class="sxs-lookup"><span data-stu-id="de0cd-106">Windows</span></span>
```
Set-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-TypeHandlerVersion] <String>]
 -ValidationPem <String> [-ClientRb <String>] [-BootstrapOptions <String>] [-JsonAttribute <String>]
 [-ChefDaemonInterval <String>] [-Daemon <String>] [-Secret <String>] [-SecretFile <String>]
 [-RunList <String>] [-ChefServerUrl <String>] [-ValidationClientName <String>] [-OrganizationName <String>]
 [-BootstrapVersion <String>] [-Windows] [[-Location] <String>] [[-Name] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de0cd-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="de0cd-107">DESCRIPTION</span></span>
<span data-ttu-id="de0cd-108">O cmdlet **set-AzVMChefExtension** adiciona a extensão chefe à máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="de0cd-108">The **Set-AzVMChefExtension** cmdlet adds the Chef extension to the virtual machine.</span></span>

## <span data-ttu-id="de0cd-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="de0cd-109">EXAMPLES</span></span>

### <span data-ttu-id="de0cd-110">Exemplo 1: adicionar uma extensão chefe a um computador virtual do Windows</span><span class="sxs-lookup"><span data-stu-id="de0cd-110">Example 1: Add a Chef extension to a Windows virtual machine</span></span>
```
PS C:\> Set-AzVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -ValidationPem "C:\my-org-validator.pem" -ClientRb "C:\client.rb" -RunList "Apache" -Daemon "service" -SecretFile "C:\my_encrypted_data_bag_secret" -Windows
```

<span data-ttu-id="de0cd-111">Esse comando adiciona uma extensão chefe a um computador virtual do Windows chamado WindowsVM001.</span><span class="sxs-lookup"><span data-stu-id="de0cd-111">This command adds a Chef extension to a Windows virtual machine named WindowsVM001.</span></span>
<span data-ttu-id="de0cd-112">Quando a máquina virtual for iniciada, o chefe inicializará a máquina virtual para executar o Apache.</span><span class="sxs-lookup"><span data-stu-id="de0cd-112">When the virtual machine starts, Chef bootstraps the virtual machine to run Apache.</span></span>

### <span data-ttu-id="de0cd-113">Exemplo 2: adicionar uma extensão chefe a um computador virtual Linux</span><span class="sxs-lookup"><span data-stu-id="de0cd-113">Example 2: Add a Chef extension to a Linux virtual machine</span></span>
```
PS C:\> Set-AzVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -ValidationPem "C:\my-org-validator.pem" -ClientRb "C:\client.rb" -RunList "Apache" -Secret "my_secret" -Linux
```

<span data-ttu-id="de0cd-114">Esse comando adiciona uma extensão chefe a um computador virtual Linux chamado LinuxVM001.</span><span class="sxs-lookup"><span data-stu-id="de0cd-114">This command adds a Chef extension to a Linux virtual machine named LinuxVM001.</span></span>
<span data-ttu-id="de0cd-115">Quando a máquina virtual for iniciada, o chefe inicializará a máquina virtual para executar o Apache.</span><span class="sxs-lookup"><span data-stu-id="de0cd-115">When the virtual machine starts, Chef bootstraps the virtual machine to run Apache.</span></span>

### <span data-ttu-id="de0cd-116">Exemplo 3: adicionar uma extensão chefe a um computador virtual do Windows com opções de inicialização</span><span class="sxs-lookup"><span data-stu-id="de0cd-116">Example 3: Add a Chef extension to a Windows virtual machine with bootstrap options</span></span>
```
PS C:\> Set-AzVMChefExtension -ResourceGroupName "ResourceGroup003" -VMName "WindowsVM002" -ValidationPem C:\my-org-validator.pem -ClientRb C:\client.rb -BootstrapOptions '{"chef_node_name":"your_node_name","chef_server_url":"https://api.opscode.com/organizations/some-org", "validation_client_name":"some-org-validator"}' -RunList "Apache" -Windows
```

<span data-ttu-id="de0cd-117">Esse comando adiciona a extensão chefe a um computador virtual do Windows chamado WindowsVM002.</span><span class="sxs-lookup"><span data-stu-id="de0cd-117">This command adds the Chef extension to a Windows virtual machine named WindowsVM002.</span></span>
<span data-ttu-id="de0cd-118">Quando a máquina virtual for iniciada, o chefe inicializará a máquina virtual para executar o Apache.</span><span class="sxs-lookup"><span data-stu-id="de0cd-118">When the virtual machine starts, Chef bootstraps the virtual machine to run Apache.</span></span>
<span data-ttu-id="de0cd-119">Após a inicialização, a máquina virtual refere-se à Bootstrapoptions especificada no formato JSON.</span><span class="sxs-lookup"><span data-stu-id="de0cd-119">After bootstrapping, the virtual machine refers to the BootstrapOptions specified in JSON format.</span></span>

## <span data-ttu-id="de0cd-120">OS</span><span class="sxs-lookup"><span data-stu-id="de0cd-120">PARAMETERS</span></span>

### <span data-ttu-id="de0cd-121">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="de0cd-121">-AutoUpgradeMinorVersion</span></span>
```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de0cd-122">-Bootstrapoptions</span><span class="sxs-lookup"><span data-stu-id="de0cd-122">-BootstrapOptions</span></span>
<span data-ttu-id="de0cd-123">Especifica as definições de configuração na opção client_rb.</span><span class="sxs-lookup"><span data-stu-id="de0cd-123">Specifies configuration settings in the client_rb option.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de0cd-124">-BootstrapVersion</span><span class="sxs-lookup"><span data-stu-id="de0cd-124">-BootstrapVersion</span></span>
<span data-ttu-id="de0cd-125">Especifica a versão da configuração de inicialização.</span><span class="sxs-lookup"><span data-stu-id="de0cd-125">Specifies the version of the bootstrap configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de0cd-126">-ChefDaemonInterval</span><span class="sxs-lookup"><span data-stu-id="de0cd-126">-ChefDaemonInterval</span></span>
<span data-ttu-id="de0cd-127">Especifica a frequência (em minutos) em que o chefe-serviço é executado.</span><span class="sxs-lookup"><span data-stu-id="de0cd-127">Specifies the frequency (in minutes) at which the chef-service runs.</span></span> <span data-ttu-id="de0cd-128">Se, caso não queira que o chefe-serviço seja instalado na máquina virtual do Azure, defina o valor como 0 nesse campo.</span><span class="sxs-lookup"><span data-stu-id="de0cd-128">If in case you don't want the chef-service to be installed on the Azure VM then set value as 0 in this field.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ChefServiceInterval

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de0cd-129">-ChefServerUrl</span><span class="sxs-lookup"><span data-stu-id="de0cd-129">-ChefServerUrl</span></span>
<span data-ttu-id="de0cd-130">Especifica o link do servidor chefe como uma URL.</span><span class="sxs-lookup"><span data-stu-id="de0cd-130">Specifies the Chef server link, as a URL.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de0cd-131">-ClientRb</span><span class="sxs-lookup"><span data-stu-id="de0cd-131">-ClientRb</span></span>
<span data-ttu-id="de0cd-132">Especifica o caminho completo do chefe cliente. rb.</span><span class="sxs-lookup"><span data-stu-id="de0cd-132">Specifies the full path of the Chef client.rb.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de0cd-133">-Daemon</span><span class="sxs-lookup"><span data-stu-id="de0cd-133">-Daemon</span></span>
<span data-ttu-id="de0cd-134">Configura o serviço chefe-cliente para execução automática.</span><span class="sxs-lookup"><span data-stu-id="de0cd-134">Configures the chef-client service for unattended execution.</span></span> <span data-ttu-id="de0cd-135">A plataforma do nó deve ser Windows.</span><span class="sxs-lookup"><span data-stu-id="de0cd-135">The node platform should be Windows.</span></span>
<span data-ttu-id="de0cd-136">Opções permitidas: ' none ', ' Service ' e ' Task '.</span><span class="sxs-lookup"><span data-stu-id="de0cd-136">Allowed options: 'none','service' and 'task'.</span></span>
<span data-ttu-id="de0cd-137">None-atualmente impede que o serviço chefe-cliente seja configurado como um serviço.</span><span class="sxs-lookup"><span data-stu-id="de0cd-137">none - Currently prevents the chef-client service from being configured as a service.</span></span>
<span data-ttu-id="de0cd-138">serviço-configura o chefe-cliente para ser executado automaticamente em segundo plano como um serviço.</span><span class="sxs-lookup"><span data-stu-id="de0cd-138">service - Configures the chef-client to run automatically in the background as a service.</span></span>
<span data-ttu-id="de0cd-139">tarefa-configura o chefe-cliente para ser executado automaticamente em segundo plano como uma tarefa agendada.</span><span class="sxs-lookup"><span data-stu-id="de0cd-139">task - Configures the chef-client to run automatically in the background as a scheduled task.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: none, service, task

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de0cd-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de0cd-140">-DefaultProfile</span></span>
<span data-ttu-id="de0cd-141">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="de0cd-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de0cd-142">-Jsonattribute</span><span class="sxs-lookup"><span data-stu-id="de0cd-142">-JsonAttribute</span></span>
<span data-ttu-id="de0cd-143">Uma cadeia de caracteres JSON a ser adicionada à primeira execução do chefe-cliente.</span><span class="sxs-lookup"><span data-stu-id="de0cd-143">A JSON string to be added to the first run of chef-client.</span></span> <span data-ttu-id="de0cd-144">por exemplo:-Jsonattribute ' {"foo": "barra"} '</span><span class="sxs-lookup"><span data-stu-id="de0cd-144">e.g. -JsonAttribute '{"foo" : "bar"}'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de0cd-145">-Linux</span><span class="sxs-lookup"><span data-stu-id="de0cd-145">-Linux</span></span>
<span data-ttu-id="de0cd-146">Indica que esse cmdlet cria um computador virtual do Windows.</span><span class="sxs-lookup"><span data-stu-id="de0cd-146">Indicates that this cmdlet creates a Windows virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Linux
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de0cd-147">-Local</span><span class="sxs-lookup"><span data-stu-id="de0cd-147">-Location</span></span>
<span data-ttu-id="de0cd-148">Especifica o local da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="de0cd-148">Specifies the location of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de0cd-149">-Nome</span><span class="sxs-lookup"><span data-stu-id="de0cd-149">-Name</span></span>
<span data-ttu-id="de0cd-150">Especifica o nome da extensão do chefe.</span><span class="sxs-lookup"><span data-stu-id="de0cd-150">Specifies the name of the Chef extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de0cd-151">-Nowait</span><span class="sxs-lookup"><span data-stu-id="de0cd-151">-NoWait</span></span>
<span data-ttu-id="de0cd-152">Inicia a operação e retorna imediatamente, antes que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="de0cd-152">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="de0cd-153">Para determinar se a operação foi concluída com êxito, use outro mecanismo.</span><span class="sxs-lookup"><span data-stu-id="de0cd-153">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de0cd-154">-OrganizationName</span><span class="sxs-lookup"><span data-stu-id="de0cd-154">-OrganizationName</span></span>
<span data-ttu-id="de0cd-155">Especifica o nome da organização da extensão chefe.</span><span class="sxs-lookup"><span data-stu-id="de0cd-155">Specifies the organization name of the Chef extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de0cd-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de0cd-156">-ResourceGroupName</span></span>
<span data-ttu-id="de0cd-157">Especifica o nome do grupo de recursos que contém a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="de0cd-157">Specifies the name of the resource group that contains the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de0cd-158">-RunList</span><span class="sxs-lookup"><span data-stu-id="de0cd-158">-RunList</span></span>
<span data-ttu-id="de0cd-159">Especifica a lista de execução do nó chefe.</span><span class="sxs-lookup"><span data-stu-id="de0cd-159">Specifies the Chef node run list.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de0cd-160">-Segredo</span><span class="sxs-lookup"><span data-stu-id="de0cd-160">-Secret</span></span>
<span data-ttu-id="de0cd-161">A chave de criptografia usada para criptografar e descriptografar os valores de item do conjunto de dados.</span><span class="sxs-lookup"><span data-stu-id="de0cd-161">The encryption key used to encrypt and decrypt the data bag item values.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de0cd-162">-Secretfile</span><span class="sxs-lookup"><span data-stu-id="de0cd-162">-SecretFile</span></span>
<span data-ttu-id="de0cd-163">O caminho para o arquivo que contém a chave de criptografia usada para criptografar e descriptografar os valores de item do conjunto de dados.</span><span class="sxs-lookup"><span data-stu-id="de0cd-163">The path to the file that contains the encryption key used to encrypt and decrypt the data bag item values.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de0cd-164">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="de0cd-164">-TypeHandlerVersion</span></span>
<span data-ttu-id="de0cd-165">Especifica a versão da extensão a ser usada para esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="de0cd-165">Specifies the version of the extension to use for this virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de0cd-166">-ValidationClientName</span><span class="sxs-lookup"><span data-stu-id="de0cd-166">-ValidationClientName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de0cd-167">-ValidationPem</span><span class="sxs-lookup"><span data-stu-id="de0cd-167">-ValidationPem</span></span>
<span data-ttu-id="de0cd-168">Especifica o caminho do arquivo. PEM do chefe Validator</span><span class="sxs-lookup"><span data-stu-id="de0cd-168">Specifies the Chef validator .pem file path</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de0cd-169">-VMName</span><span class="sxs-lookup"><span data-stu-id="de0cd-169">-VMName</span></span>
<span data-ttu-id="de0cd-170">Especifica o nome de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="de0cd-170">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="de0cd-171">Esse cmdlet adiciona a extensão chefe para a máquina virtual que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="de0cd-171">This cmdlet adds the Chef extension for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de0cd-172">-Windows</span><span class="sxs-lookup"><span data-stu-id="de0cd-172">-Windows</span></span>
<span data-ttu-id="de0cd-173">Indica que esse cmdlet cria um computador virtual do Windows.</span><span class="sxs-lookup"><span data-stu-id="de0cd-173">Indicates that this cmdlet creates a Windows virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de0cd-174">-Confirme</span><span class="sxs-lookup"><span data-stu-id="de0cd-174">-Confirm</span></span>
<span data-ttu-id="de0cd-175">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de0cd-175">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de0cd-176">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de0cd-176">-WhatIf</span></span>
<span data-ttu-id="de0cd-177">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="de0cd-177">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de0cd-178">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="de0cd-178">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de0cd-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de0cd-179">CommonParameters</span></span>
<span data-ttu-id="de0cd-180">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de0cd-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de0cd-181">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="de0cd-181">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de0cd-182">SENSORES</span><span class="sxs-lookup"><span data-stu-id="de0cd-182">INPUTS</span></span>

### <span data-ttu-id="de0cd-183">System. String</span><span class="sxs-lookup"><span data-stu-id="de0cd-183">System.String</span></span>

### <span data-ttu-id="de0cd-184">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="de0cd-184">System.Boolean</span></span>

## <span data-ttu-id="de0cd-185">EXIBE</span><span class="sxs-lookup"><span data-stu-id="de0cd-185">OUTPUTS</span></span>

### <span data-ttu-id="de0cd-186">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="de0cd-186">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="de0cd-187">INFORMA</span><span class="sxs-lookup"><span data-stu-id="de0cd-187">NOTES</span></span>

## <span data-ttu-id="de0cd-188">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="de0cd-188">RELATED LINKS</span></span>

[<span data-ttu-id="de0cd-189">Get-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="de0cd-189">Get-AzVMChefExtension</span></span>](./Get-AzVMChefExtension.md)

[<span data-ttu-id="de0cd-190">Remove-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="de0cd-190">Remove-AzVMChefExtension</span></span>](./Remove-AzVMChefExtension.md)
