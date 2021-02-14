---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: CC306D8C-A5EE-4655-B686-E5A77CCE5042
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmchefextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMChefExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMChefExtension.md
ms.openlocfilehash: 2821e9404fe4101415aa04a8b0d331b3066563df
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111086"
---
# <span data-ttu-id="2cb87-101">Set-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="2cb87-101">Set-AzVMChefExtension</span></span>

## <span data-ttu-id="2cb87-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2cb87-102">SYNOPSIS</span></span>
<span data-ttu-id="2cb87-103">Adiciona uma extensão Descarros a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="2cb87-103">Adds a Chef extension to a virtual machine.</span></span>

## <span data-ttu-id="2cb87-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2cb87-104">SYNTAX</span></span>

### <span data-ttu-id="2cb87-105">Linux</span><span class="sxs-lookup"><span data-stu-id="2cb87-105">Linux</span></span>
```
Set-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-TypeHandlerVersion] <String>]
 -ValidationPem <String> [-ClientRb <String>] [-BootstrapOptions <String>] [-JsonAttribute <String>]
 [-ChefDaemonInterval <String>] [-Daemon <String>] [-Secret <String>] [-SecretFile <String>]
 [-RunList <String>] [-ChefServerUrl <String>] [-ValidationClientName <String>] [-OrganizationName <String>]
 [-BootstrapVersion <String>] [-Linux] [[-Location] <String>] [[-Name] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2cb87-106">Windows</span><span class="sxs-lookup"><span data-stu-id="2cb87-106">Windows</span></span>
```
Set-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-TypeHandlerVersion] <String>]
 -ValidationPem <String> [-ClientRb <String>] [-BootstrapOptions <String>] [-JsonAttribute <String>]
 [-ChefDaemonInterval <String>] [-Daemon <String>] [-Secret <String>] [-SecretFile <String>]
 [-RunList <String>] [-ChefServerUrl <String>] [-ValidationClientName <String>] [-OrganizationName <String>]
 [-BootstrapVersion <String>] [-Windows] [[-Location] <String>] [[-Name] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2cb87-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="2cb87-107">DESCRIPTION</span></span>
<span data-ttu-id="2cb87-108">O **cmdlet Set-AzVM Eletension** adiciona a extensão Desarmada à máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="2cb87-108">The **Set-AzVMChefExtension** cmdlet adds the Chef extension to the virtual machine.</span></span>

## <span data-ttu-id="2cb87-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2cb87-109">EXAMPLES</span></span>

### <span data-ttu-id="2cb87-110">Exemplo 1: Adicionar uma extensão Desarmados a uma máquina virtual do Windows</span><span class="sxs-lookup"><span data-stu-id="2cb87-110">Example 1: Add a Chef extension to a Windows virtual machine</span></span>
```
PS C:\> Set-AzVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -ValidationPem "C:\my-org-validator.pem" -ClientRb "C:\client.rb" -RunList "Apache" -Daemon "service" -SecretFile "C:\my_encrypted_data_bag_secret" -Windows
```

<span data-ttu-id="2cb87-111">Este comando adiciona uma extensão Descarada a uma máquina virtual do Windows chamada WindowsVM001.</span><span class="sxs-lookup"><span data-stu-id="2cb87-111">This command adds a Chef extension to a Windows virtual machine named WindowsVM001.</span></span>
<span data-ttu-id="2cb87-112">Quando a máquina virtual é iniciada, o Boots insocará a máquina virtual para executar o Apache.</span><span class="sxs-lookup"><span data-stu-id="2cb87-112">When the virtual machine starts, Chef bootstraps the virtual machine to run Apache.</span></span>

### <span data-ttu-id="2cb87-113">Exemplo 2: Adicionar uma extensão Desarm a uma máquina virtual do Linux</span><span class="sxs-lookup"><span data-stu-id="2cb87-113">Example 2: Add a Chef extension to a Linux virtual machine</span></span>
```
PS C:\> Set-AzVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -ValidationPem "C:\my-org-validator.pem" -ClientRb "C:\client.rb" -RunList "Apache" -Secret "my_secret" -Linux
```

<span data-ttu-id="2cb87-114">Este comando adiciona uma extensão Desarme a uma máquina virtual do Linux chamada LinuxVM001.</span><span class="sxs-lookup"><span data-stu-id="2cb87-114">This command adds a Chef extension to a Linux virtual machine named LinuxVM001.</span></span>
<span data-ttu-id="2cb87-115">Quando a máquina virtual é iniciada, Bootstraps a máquina virtual para executar Apache.</span><span class="sxs-lookup"><span data-stu-id="2cb87-115">When the virtual machine starts, Chef bootstraps the virtual machine to run Apache.</span></span>

### <span data-ttu-id="2cb87-116">Exemplo 3: Adicionar uma extensão Descarada a uma máquina virtual do Windows com opções de bootstrap</span><span class="sxs-lookup"><span data-stu-id="2cb87-116">Example 3: Add a Chef extension to a Windows virtual machine with bootstrap options</span></span>
```
PS C:\> Set-AzVMChefExtension -ResourceGroupName "ResourceGroup003" -VMName "WindowsVM002" -ValidationPem C:\my-org-validator.pem -ClientRb C:\client.rb -BootstrapOptions '{"chef_node_name":"your_node_name","chef_server_url":"https://api.opscode.com/organizations/some-org", "validation_client_name":"some-org-validator"}' -RunList "Apache" -Windows
```

<span data-ttu-id="2cb87-117">Esse comando adiciona a extensão Desarme a uma máquina virtual do Windows chamada WindowsVM002.</span><span class="sxs-lookup"><span data-stu-id="2cb87-117">This command adds the Chef extension to a Windows virtual machine named WindowsVM002.</span></span>
<span data-ttu-id="2cb87-118">Quando a máquina virtual é iniciada, o Boots insocará a máquina virtual para executar o Apache.</span><span class="sxs-lookup"><span data-stu-id="2cb87-118">When the virtual machine starts, Chef bootstraps the virtual machine to run Apache.</span></span>
<span data-ttu-id="2cb87-119">Após a inicialização, a máquina virtual se refere às BootstrapOptions especificadas no formato JSON.</span><span class="sxs-lookup"><span data-stu-id="2cb87-119">After bootstrapping, the virtual machine refers to the BootstrapOptions specified in JSON format.</span></span>

## <span data-ttu-id="2cb87-120">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2cb87-120">PARAMETERS</span></span>

### <span data-ttu-id="2cb87-121">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="2cb87-121">-AutoUpgradeMinorVersion</span></span>
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

### <span data-ttu-id="2cb87-122">-BootstrapOptions</span><span class="sxs-lookup"><span data-stu-id="2cb87-122">-BootstrapOptions</span></span>
<span data-ttu-id="2cb87-123">Especifica as configurações de configuração na client_rb opção.</span><span class="sxs-lookup"><span data-stu-id="2cb87-123">Specifies configuration settings in the client_rb option.</span></span>

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

### <span data-ttu-id="2cb87-124">-BootstrapVersion</span><span class="sxs-lookup"><span data-stu-id="2cb87-124">-BootstrapVersion</span></span>
<span data-ttu-id="2cb87-125">Especifica a versão da configuração de bootstrap.</span><span class="sxs-lookup"><span data-stu-id="2cb87-125">Specifies the version of the bootstrap configuration.</span></span>

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

### <span data-ttu-id="2cb87-126">-HeiDaemonInterval</span><span class="sxs-lookup"><span data-stu-id="2cb87-126">-ChefDaemonInterval</span></span>
<span data-ttu-id="2cb87-127">Especifica a frequência (em minutos) na qual o serviço é executado.</span><span class="sxs-lookup"><span data-stu-id="2cb87-127">Specifies the frequency (in minutes) at which the chef-service runs.</span></span> <span data-ttu-id="2cb87-128">Se, no caso de você não quiser que o serviço seja instalado no VM do Azure, deverão definir o valor como 0 nesse campo.</span><span class="sxs-lookup"><span data-stu-id="2cb87-128">If in case you don't want the chef-service to be installed on the Azure VM then set value as 0 in this field.</span></span>

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

### <span data-ttu-id="2cb87-129">-PorteserverUrl</span><span class="sxs-lookup"><span data-stu-id="2cb87-129">-ChefServerUrl</span></span>
<span data-ttu-id="2cb87-130">Especifica o link do servidor Descarrém, como uma URL.</span><span class="sxs-lookup"><span data-stu-id="2cb87-130">Specifies the Chef server link, as a URL.</span></span>

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

### <span data-ttu-id="2cb87-131">-ClientRb</span><span class="sxs-lookup"><span data-stu-id="2cb87-131">-ClientRb</span></span>
<span data-ttu-id="2cb87-132">Especifica o caminho completo do cliente Deca.rb.</span><span class="sxs-lookup"><span data-stu-id="2cb87-132">Specifies the full path of the Chef client.rb.</span></span>

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

### <span data-ttu-id="2cb87-133">-Daemon</span><span class="sxs-lookup"><span data-stu-id="2cb87-133">-Daemon</span></span>
<span data-ttu-id="2cb87-134">Configura o serviço de cliente-chefe para execução autônoma.</span><span class="sxs-lookup"><span data-stu-id="2cb87-134">Configures the chef-client service for unattended execution.</span></span> <span data-ttu-id="2cb87-135">A plataforma de nó deve ser o Windows.</span><span class="sxs-lookup"><span data-stu-id="2cb87-135">The node platform should be Windows.</span></span>
<span data-ttu-id="2cb87-136">Opções permitidas: 'nenhum', 'serviço' e 'tarefa'.</span><span class="sxs-lookup"><span data-stu-id="2cb87-136">Allowed options: 'none','service' and 'task'.</span></span>
<span data-ttu-id="2cb87-137">nenhum – atualmente impede que o serviço de cliente-de-cliente seja configurado como um serviço.</span><span class="sxs-lookup"><span data-stu-id="2cb87-137">none - Currently prevents the chef-client service from being configured as a service.</span></span>
<span data-ttu-id="2cb87-138">serviço – configura o cliente-chefe para ser executado automaticamente em segundo plano como um serviço.</span><span class="sxs-lookup"><span data-stu-id="2cb87-138">service - Configures the chef-client to run automatically in the background as a service.</span></span>
<span data-ttu-id="2cb87-139">tarefa – configura o cliente-chefe para ser executado automaticamente em segundo plano como uma tarefa agendada.</span><span class="sxs-lookup"><span data-stu-id="2cb87-139">task - Configures the chef-client to run automatically in the background as a scheduled task.</span></span>

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

### <span data-ttu-id="2cb87-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cb87-140">-DefaultProfile</span></span>
<span data-ttu-id="2cb87-141">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="2cb87-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2cb87-142">-JsonAttribute</span><span class="sxs-lookup"><span data-stu-id="2cb87-142">-JsonAttribute</span></span>
<span data-ttu-id="2cb87-143">Uma cadeia de caracteres JSON a ser adicionada à primeira executar do cliente-chefe.</span><span class="sxs-lookup"><span data-stu-id="2cb87-143">A JSON string to be added to the first run of chef-client.</span></span> <span data-ttu-id="2cb87-144">por exemplo, -JsonAttribute '{"foo" : "bar"}'</span><span class="sxs-lookup"><span data-stu-id="2cb87-144">e.g. -JsonAttribute '{"foo" : "bar"}'</span></span>

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

### <span data-ttu-id="2cb87-145">-Linux</span><span class="sxs-lookup"><span data-stu-id="2cb87-145">-Linux</span></span>
<span data-ttu-id="2cb87-146">Indica que esse cmdlet cria uma máquina virtual do Windows.</span><span class="sxs-lookup"><span data-stu-id="2cb87-146">Indicates that this cmdlet creates a Windows virtual machine.</span></span>

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

### <span data-ttu-id="2cb87-147">-Local</span><span class="sxs-lookup"><span data-stu-id="2cb87-147">-Location</span></span>
<span data-ttu-id="2cb87-148">Especifica a localização da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="2cb87-148">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="2cb87-149">-Nome</span><span class="sxs-lookup"><span data-stu-id="2cb87-149">-Name</span></span>
<span data-ttu-id="2cb87-150">Especifica o nome da extensão Deeira.</span><span class="sxs-lookup"><span data-stu-id="2cb87-150">Specifies the name of the Chef extension.</span></span>

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

### <span data-ttu-id="2cb87-151">-NoWait</span><span class="sxs-lookup"><span data-stu-id="2cb87-151">-NoWait</span></span>
<span data-ttu-id="2cb87-152">Inicia a operação e retorna imediatamente, antes que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="2cb87-152">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="2cb87-153">Para determinar se a operação foi concluída com êxito, use algum outro mecanismo.</span><span class="sxs-lookup"><span data-stu-id="2cb87-153">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="2cb87-154">-OrganizationName</span><span class="sxs-lookup"><span data-stu-id="2cb87-154">-OrganizationName</span></span>
<span data-ttu-id="2cb87-155">Especifica o nome da organização da extensão Deda.</span><span class="sxs-lookup"><span data-stu-id="2cb87-155">Specifies the organization name of the Chef extension.</span></span>

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

### <span data-ttu-id="2cb87-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2cb87-156">-ResourceGroupName</span></span>
<span data-ttu-id="2cb87-157">Especifica o nome do grupo de recursos que contém a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="2cb87-157">Specifies the name of the resource group that contains the virtual machine.</span></span>

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

### <span data-ttu-id="2cb87-158">-RunList</span><span class="sxs-lookup"><span data-stu-id="2cb87-158">-RunList</span></span>
<span data-ttu-id="2cb87-159">Especifica a lista de executar nó Descaro.</span><span class="sxs-lookup"><span data-stu-id="2cb87-159">Specifies the Chef node run list.</span></span>

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

### <span data-ttu-id="2cb87-160">-Secret</span><span class="sxs-lookup"><span data-stu-id="2cb87-160">-Secret</span></span>
<span data-ttu-id="2cb87-161">A chave de criptografia usada para criptografar e descriptografar os valores do item do pacote de dados.</span><span class="sxs-lookup"><span data-stu-id="2cb87-161">The encryption key used to encrypt and decrypt the data bag item values.</span></span>

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

### <span data-ttu-id="2cb87-162">-SecretFile</span><span class="sxs-lookup"><span data-stu-id="2cb87-162">-SecretFile</span></span>
<span data-ttu-id="2cb87-163">O caminho para o arquivo que contém a chave de criptografia usada para criptografar e descriptografar os valores do item do pacote de dados.</span><span class="sxs-lookup"><span data-stu-id="2cb87-163">The path to the file that contains the encryption key used to encrypt and decrypt the data bag item values.</span></span>

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

### <span data-ttu-id="2cb87-164">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="2cb87-164">-TypeHandlerVersion</span></span>
<span data-ttu-id="2cb87-165">Especifica a versão da extensão a ser usada para esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="2cb87-165">Specifies the version of the extension to use for this virtual machine.</span></span>

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

### <span data-ttu-id="2cb87-166">-ValidationClientName</span><span class="sxs-lookup"><span data-stu-id="2cb87-166">-ValidationClientName</span></span>
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

### <span data-ttu-id="2cb87-167">-ValidationPem</span><span class="sxs-lookup"><span data-stu-id="2cb87-167">-ValidationPem</span></span>
<span data-ttu-id="2cb87-168">Especifica o caminho de arquivo .pem do validador .pem</span><span class="sxs-lookup"><span data-stu-id="2cb87-168">Specifies the Chef validator .pem file path</span></span>

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

### <span data-ttu-id="2cb87-169">-VMName</span><span class="sxs-lookup"><span data-stu-id="2cb87-169">-VMName</span></span>
<span data-ttu-id="2cb87-170">Especifica o nome de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="2cb87-170">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="2cb87-171">Este cmdlet adiciona a extensão Deeira para a máquina virtual especificada por este parâmetro.</span><span class="sxs-lookup"><span data-stu-id="2cb87-171">This cmdlet adds the Chef extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="2cb87-172">-Windows</span><span class="sxs-lookup"><span data-stu-id="2cb87-172">-Windows</span></span>
<span data-ttu-id="2cb87-173">Indica que esse cmdlet cria uma máquina virtual do Windows.</span><span class="sxs-lookup"><span data-stu-id="2cb87-173">Indicates that this cmdlet creates a Windows virtual machine.</span></span>

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

### <span data-ttu-id="2cb87-174">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="2cb87-174">-Confirm</span></span>
<span data-ttu-id="2cb87-175">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2cb87-175">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2cb87-176">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2cb87-176">-WhatIf</span></span>
<span data-ttu-id="2cb87-177">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="2cb87-177">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2cb87-178">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2cb87-178">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2cb87-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cb87-179">CommonParameters</span></span>
<span data-ttu-id="2cb87-180">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2cb87-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cb87-181">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2cb87-181">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cb87-182">Entradas</span><span class="sxs-lookup"><span data-stu-id="2cb87-182">INPUTS</span></span>

### <span data-ttu-id="2cb87-183">System.String</span><span class="sxs-lookup"><span data-stu-id="2cb87-183">System.String</span></span>

### <span data-ttu-id="2cb87-184">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2cb87-184">System.Boolean</span></span>

## <span data-ttu-id="2cb87-185">Saídas</span><span class="sxs-lookup"><span data-stu-id="2cb87-185">OUTPUTS</span></span>

### <span data-ttu-id="2cb87-186">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="2cb87-186">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="2cb87-187">Notas</span><span class="sxs-lookup"><span data-stu-id="2cb87-187">NOTES</span></span>

## <span data-ttu-id="2cb87-188">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2cb87-188">RELATED LINKS</span></span>

[<span data-ttu-id="2cb87-189">Get-AzVM Eletension</span><span class="sxs-lookup"><span data-stu-id="2cb87-189">Get-AzVMChefExtension</span></span>](./Get-AzVMChefExtension.md)

[<span data-ttu-id="2cb87-190">Remove-AzVM Eletension</span><span class="sxs-lookup"><span data-stu-id="2cb87-190">Remove-AzVMChefExtension</span></span>](./Remove-AzVMChefExtension.md)
