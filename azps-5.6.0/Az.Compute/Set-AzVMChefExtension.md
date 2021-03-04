---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: CC306D8C-A5EE-4655-B686-E5A77CCE5042
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmchefextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMChefExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMChefExtension.md
ms.openlocfilehash: 2e0aeb7535f07e9841c9c0a35a131ce0ca7b1a57
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887896"
---
# <span data-ttu-id="f5eea-101">Set-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="f5eea-101">Set-AzVMChefExtension</span></span>

## <span data-ttu-id="f5eea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5eea-102">SYNOPSIS</span></span>
<span data-ttu-id="f5eea-103">Adiciona uma extensão do Chefe a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="f5eea-103">Adds a Chef extension to a virtual machine.</span></span>

## <span data-ttu-id="f5eea-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f5eea-104">SYNTAX</span></span>

### <span data-ttu-id="f5eea-105">Linux</span><span class="sxs-lookup"><span data-stu-id="f5eea-105">Linux</span></span>
```
Set-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-TypeHandlerVersion] <String>]
 -ValidationPem <String> [-ClientRb <String>] [-BootstrapOptions <String>] [-JsonAttribute <String>]
 [-ChefDaemonInterval <String>] [-Daemon <String>] [-Secret <String>] [-SecretFile <String>]
 [-RunList <String>] [-ChefServerUrl <String>] [-ValidationClientName <String>] [-OrganizationName <String>]
 [-BootstrapVersion <String>] [-Linux] [[-Location] <String>] [[-Name] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5eea-106">Windows</span><span class="sxs-lookup"><span data-stu-id="f5eea-106">Windows</span></span>
```
Set-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-TypeHandlerVersion] <String>]
 -ValidationPem <String> [-ClientRb <String>] [-BootstrapOptions <String>] [-JsonAttribute <String>]
 [-ChefDaemonInterval <String>] [-Daemon <String>] [-Secret <String>] [-SecretFile <String>]
 [-RunList <String>] [-ChefServerUrl <String>] [-ValidationClientName <String>] [-OrganizationName <String>]
 [-BootstrapVersion <String>] [-Windows] [[-Location] <String>] [[-Name] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5eea-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f5eea-107">DESCRIPTION</span></span>
<span data-ttu-id="f5eea-108">O cmdlet **Set-AzVMChefExtension** adiciona a extensão do Chefe à máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="f5eea-108">The **Set-AzVMChefExtension** cmdlet adds the Chef extension to the virtual machine.</span></span>

## <span data-ttu-id="f5eea-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f5eea-109">EXAMPLES</span></span>

### <span data-ttu-id="f5eea-110">Exemplo 1: Adicionar uma extensão do Chefe a uma máquina virtual do Windows</span><span class="sxs-lookup"><span data-stu-id="f5eea-110">Example 1: Add a Chef extension to a Windows virtual machine</span></span>
```
PS C:\> Set-AzVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -ValidationPem "C:\my-org-validator.pem" -ClientRb "C:\client.rb" -RunList "Apache" -Daemon "service" -SecretFile "C:\my_encrypted_data_bag_secret" -Windows
```

<span data-ttu-id="f5eea-111">Este comando adiciona uma extensão do Chefe a uma máquina virtual do Windows chamada WindowsVM001.</span><span class="sxs-lookup"><span data-stu-id="f5eea-111">This command adds a Chef extension to a Windows virtual machine named WindowsVM001.</span></span>
<span data-ttu-id="f5eea-112">Quando a máquina virtual é iniciada, o Chefe inicializa a máquina virtual para executar o Apache.</span><span class="sxs-lookup"><span data-stu-id="f5eea-112">When the virtual machine starts, Chef bootstraps the virtual machine to run Apache.</span></span>

### <span data-ttu-id="f5eea-113">Exemplo 2: Adicionar uma extensão do Chefe a uma máquina virtual Linux</span><span class="sxs-lookup"><span data-stu-id="f5eea-113">Example 2: Add a Chef extension to a Linux virtual machine</span></span>
```
PS C:\> Set-AzVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -ValidationPem "C:\my-org-validator.pem" -ClientRb "C:\client.rb" -RunList "Apache" -Secret "my_secret" -Linux
```

<span data-ttu-id="f5eea-114">Este comando adiciona uma extensão do Chefe a uma máquina virtual Linux chamada LinuxVM001.</span><span class="sxs-lookup"><span data-stu-id="f5eea-114">This command adds a Chef extension to a Linux virtual machine named LinuxVM001.</span></span>
<span data-ttu-id="f5eea-115">Quando a máquina virtual é iniciada, o Chefe inicializa a máquina virtual para executar o Apache.</span><span class="sxs-lookup"><span data-stu-id="f5eea-115">When the virtual machine starts, Chef bootstraps the virtual machine to run Apache.</span></span>

### <span data-ttu-id="f5eea-116">Exemplo 3: Adicionar uma extensão do Chefe a uma máquina virtual do Windows com opções de bootstrap</span><span class="sxs-lookup"><span data-stu-id="f5eea-116">Example 3: Add a Chef extension to a Windows virtual machine with bootstrap options</span></span>
```
PS C:\> Set-AzVMChefExtension -ResourceGroupName "ResourceGroup003" -VMName "WindowsVM002" -ValidationPem C:\my-org-validator.pem -ClientRb C:\client.rb -BootstrapOptions '{"chef_node_name":"your_node_name","chef_server_url":"https://api.opscode.com/organizations/some-org", "validation_client_name":"some-org-validator"}' -RunList "Apache" -Windows
```

<span data-ttu-id="f5eea-117">Este comando adiciona a extensão do Chefe a uma máquina virtual do Windows chamada WindowsVM002.</span><span class="sxs-lookup"><span data-stu-id="f5eea-117">This command adds the Chef extension to a Windows virtual machine named WindowsVM002.</span></span>
<span data-ttu-id="f5eea-118">Quando a máquina virtual é iniciada, o Chefe inicializa a máquina virtual para executar o Apache.</span><span class="sxs-lookup"><span data-stu-id="f5eea-118">When the virtual machine starts, Chef bootstraps the virtual machine to run Apache.</span></span>
<span data-ttu-id="f5eea-119">Após a inicialização, a máquina virtual se refere às BootstrapOptions especificadas no formato JSON.</span><span class="sxs-lookup"><span data-stu-id="f5eea-119">After bootstrapping, the virtual machine refers to the BootstrapOptions specified in JSON format.</span></span>

## <span data-ttu-id="f5eea-120">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f5eea-120">PARAMETERS</span></span>

### <span data-ttu-id="f5eea-121">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="f5eea-121">-AutoUpgradeMinorVersion</span></span>
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

### <span data-ttu-id="f5eea-122">-BootstrapOptions</span><span class="sxs-lookup"><span data-stu-id="f5eea-122">-BootstrapOptions</span></span>
<span data-ttu-id="f5eea-123">Especifica as configurações na opção client_rb.</span><span class="sxs-lookup"><span data-stu-id="f5eea-123">Specifies configuration settings in the client_rb option.</span></span>

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

### <span data-ttu-id="f5eea-124">-BootstrapVersion</span><span class="sxs-lookup"><span data-stu-id="f5eea-124">-BootstrapVersion</span></span>
<span data-ttu-id="f5eea-125">Especifica a versão da configuração de bootstrap.</span><span class="sxs-lookup"><span data-stu-id="f5eea-125">Specifies the version of the bootstrap configuration.</span></span>

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

### <span data-ttu-id="f5eea-126">-ChefeDaemonInterval</span><span class="sxs-lookup"><span data-stu-id="f5eea-126">-ChefDaemonInterval</span></span>
<span data-ttu-id="f5eea-127">Especifica a frequência (em minutos) na qual o serviço de cozinha é executado.</span><span class="sxs-lookup"><span data-stu-id="f5eea-127">Specifies the frequency (in minutes) at which the chef-service runs.</span></span> <span data-ttu-id="f5eea-128">Se, caso você não queira que o serviço de cozinha seja instalado na VM do Azure, de definir o valor como 0 neste campo.</span><span class="sxs-lookup"><span data-stu-id="f5eea-128">If in case you don't want the chef-service to be installed on the Azure VM then set value as 0 in this field.</span></span>

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

### <span data-ttu-id="f5eea-129">-ChefeServerUrl</span><span class="sxs-lookup"><span data-stu-id="f5eea-129">-ChefServerUrl</span></span>
<span data-ttu-id="f5eea-130">Especifica o link do servidor do Chefe, como uma URL.</span><span class="sxs-lookup"><span data-stu-id="f5eea-130">Specifies the Chef server link, as a URL.</span></span>

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

### <span data-ttu-id="f5eea-131">-ClientRb</span><span class="sxs-lookup"><span data-stu-id="f5eea-131">-ClientRb</span></span>
<span data-ttu-id="f5eea-132">Especifica o caminho completo do cliente.rb do Chefe.</span><span class="sxs-lookup"><span data-stu-id="f5eea-132">Specifies the full path of the Chef client.rb.</span></span>

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

### <span data-ttu-id="f5eea-133">-Daemon</span><span class="sxs-lookup"><span data-stu-id="f5eea-133">-Daemon</span></span>
<span data-ttu-id="f5eea-134">Configura o serviço de cliente-chefe para execução autônoma.</span><span class="sxs-lookup"><span data-stu-id="f5eea-134">Configures the chef-client service for unattended execution.</span></span> <span data-ttu-id="f5eea-135">A plataforma de nó deve ser o Windows.</span><span class="sxs-lookup"><span data-stu-id="f5eea-135">The node platform should be Windows.</span></span>
<span data-ttu-id="f5eea-136">Opções permitidas: 'none','service' e 'task'.</span><span class="sxs-lookup"><span data-stu-id="f5eea-136">Allowed options: 'none','service' and 'task'.</span></span>
<span data-ttu-id="f5eea-137">none - Atualmente impede que o serviço de cliente-chefe seja configurado como um serviço.</span><span class="sxs-lookup"><span data-stu-id="f5eea-137">none - Currently prevents the chef-client service from being configured as a service.</span></span>
<span data-ttu-id="f5eea-138">service - Configura o cliente-chefe para ser executado automaticamente em segundo plano como um serviço.</span><span class="sxs-lookup"><span data-stu-id="f5eea-138">service - Configures the chef-client to run automatically in the background as a service.</span></span>
<span data-ttu-id="f5eea-139">task - Configura o chefe-cliente para ser executado automaticamente em segundo plano como uma tarefa agendada.</span><span class="sxs-lookup"><span data-stu-id="f5eea-139">task - Configures the chef-client to run automatically in the background as a scheduled task.</span></span>

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

### <span data-ttu-id="f5eea-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5eea-140">-DefaultProfile</span></span>
<span data-ttu-id="f5eea-141">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="f5eea-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f5eea-142">-JsonAttribute</span><span class="sxs-lookup"><span data-stu-id="f5eea-142">-JsonAttribute</span></span>
<span data-ttu-id="f5eea-143">Uma cadeia de caracteres JSON a ser adicionada à primeira executar do chefe-cliente.</span><span class="sxs-lookup"><span data-stu-id="f5eea-143">A JSON string to be added to the first run of chef-client.</span></span> <span data-ttu-id="f5eea-144">por exemplo, -JsonAttribute '{"foo" : "bar"}'</span><span class="sxs-lookup"><span data-stu-id="f5eea-144">e.g. -JsonAttribute '{"foo" : "bar"}'</span></span>

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

### <span data-ttu-id="f5eea-145">-Linux</span><span class="sxs-lookup"><span data-stu-id="f5eea-145">-Linux</span></span>
<span data-ttu-id="f5eea-146">Indica que esse cmdlet cria uma máquina virtual do Windows.</span><span class="sxs-lookup"><span data-stu-id="f5eea-146">Indicates that this cmdlet creates a Windows virtual machine.</span></span>

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

### <span data-ttu-id="f5eea-147">-Location</span><span class="sxs-lookup"><span data-stu-id="f5eea-147">-Location</span></span>
<span data-ttu-id="f5eea-148">Especifica o local da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="f5eea-148">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="f5eea-149">-Name</span><span class="sxs-lookup"><span data-stu-id="f5eea-149">-Name</span></span>
<span data-ttu-id="f5eea-150">Especifica o nome da extensão do Chefe.</span><span class="sxs-lookup"><span data-stu-id="f5eea-150">Specifies the name of the Chef extension.</span></span>

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

### <span data-ttu-id="f5eea-151">-NoWait</span><span class="sxs-lookup"><span data-stu-id="f5eea-151">-NoWait</span></span>
<span data-ttu-id="f5eea-152">Inicia a operação e retorna imediatamente, antes que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="f5eea-152">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="f5eea-153">Para determinar se a operação foi concluída com êxito, use algum outro mecanismo.</span><span class="sxs-lookup"><span data-stu-id="f5eea-153">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="f5eea-154">-OrganizationName</span><span class="sxs-lookup"><span data-stu-id="f5eea-154">-OrganizationName</span></span>
<span data-ttu-id="f5eea-155">Especifica o nome da organização da extensão do Chefe.</span><span class="sxs-lookup"><span data-stu-id="f5eea-155">Specifies the organization name of the Chef extension.</span></span>

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

### <span data-ttu-id="f5eea-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5eea-156">-ResourceGroupName</span></span>
<span data-ttu-id="f5eea-157">Especifica o nome do grupo de recursos que contém a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="f5eea-157">Specifies the name of the resource group that contains the virtual machine.</span></span>

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

### <span data-ttu-id="f5eea-158">-RunList</span><span class="sxs-lookup"><span data-stu-id="f5eea-158">-RunList</span></span>
<span data-ttu-id="f5eea-159">Especifica a lista de executar nó do Chefe.</span><span class="sxs-lookup"><span data-stu-id="f5eea-159">Specifies the Chef node run list.</span></span>

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

### <span data-ttu-id="f5eea-160">-Secret</span><span class="sxs-lookup"><span data-stu-id="f5eea-160">-Secret</span></span>
<span data-ttu-id="f5eea-161">A chave de criptografia usada para criptografar e descriptografar os valores do item do pacote de dados.</span><span class="sxs-lookup"><span data-stu-id="f5eea-161">The encryption key used to encrypt and decrypt the data bag item values.</span></span>

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

### <span data-ttu-id="f5eea-162">-SecretFile</span><span class="sxs-lookup"><span data-stu-id="f5eea-162">-SecretFile</span></span>
<span data-ttu-id="f5eea-163">O caminho para o arquivo que contém a chave de criptografia usada para criptografar e descriptografar os valores do item do pacote de dados.</span><span class="sxs-lookup"><span data-stu-id="f5eea-163">The path to the file that contains the encryption key used to encrypt and decrypt the data bag item values.</span></span>

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

### <span data-ttu-id="f5eea-164">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="f5eea-164">-TypeHandlerVersion</span></span>
<span data-ttu-id="f5eea-165">Especifica a versão da extensão a ser usada para essa máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="f5eea-165">Specifies the version of the extension to use for this virtual machine.</span></span>

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

### <span data-ttu-id="f5eea-166">-ValidationClientName</span><span class="sxs-lookup"><span data-stu-id="f5eea-166">-ValidationClientName</span></span>
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

### <span data-ttu-id="f5eea-167">-ValidationPem</span><span class="sxs-lookup"><span data-stu-id="f5eea-167">-ValidationPem</span></span>
<span data-ttu-id="f5eea-168">Especifica o caminho do arquivo .pem do validador do Chefe</span><span class="sxs-lookup"><span data-stu-id="f5eea-168">Specifies the Chef validator .pem file path</span></span>

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

### <span data-ttu-id="f5eea-169">-VMName</span><span class="sxs-lookup"><span data-stu-id="f5eea-169">-VMName</span></span>
<span data-ttu-id="f5eea-170">Especifica o nome de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="f5eea-170">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="f5eea-171">Este cmdlet adiciona a extensão do Chefe para a máquina virtual especificada por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="f5eea-171">This cmdlet adds the Chef extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="f5eea-172">-Windows</span><span class="sxs-lookup"><span data-stu-id="f5eea-172">-Windows</span></span>
<span data-ttu-id="f5eea-173">Indica que esse cmdlet cria uma máquina virtual do Windows.</span><span class="sxs-lookup"><span data-stu-id="f5eea-173">Indicates that this cmdlet creates a Windows virtual machine.</span></span>

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

### <span data-ttu-id="f5eea-174">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f5eea-174">-Confirm</span></span>
<span data-ttu-id="f5eea-175">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f5eea-175">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5eea-176">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5eea-176">-WhatIf</span></span>
<span data-ttu-id="f5eea-177">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f5eea-177">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5eea-178">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f5eea-178">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5eea-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5eea-179">CommonParameters</span></span>
<span data-ttu-id="f5eea-180">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5eea-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5eea-181">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f5eea-181">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5eea-182">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f5eea-182">INPUTS</span></span>

### <span data-ttu-id="f5eea-183">System.String</span><span class="sxs-lookup"><span data-stu-id="f5eea-183">System.String</span></span>

### <span data-ttu-id="f5eea-184">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f5eea-184">System.Boolean</span></span>

## <span data-ttu-id="f5eea-185">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f5eea-185">OUTPUTS</span></span>

### <span data-ttu-id="f5eea-186">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="f5eea-186">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="f5eea-187">NOTES</span><span class="sxs-lookup"><span data-stu-id="f5eea-187">NOTES</span></span>

## <span data-ttu-id="f5eea-188">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f5eea-188">RELATED LINKS</span></span>

[<span data-ttu-id="f5eea-189">Get-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="f5eea-189">Get-AzVMChefExtension</span></span>](./Get-AzVMChefExtension.md)

[<span data-ttu-id="f5eea-190">Remove-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="f5eea-190">Remove-AzVMChefExtension</span></span>](./Remove-AzVMChefExtension.md)
