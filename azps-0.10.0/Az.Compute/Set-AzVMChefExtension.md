---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: CC306D8C-A5EE-4655-B686-E5A77CCE5042
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmchefextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMChefExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMChefExtension.md
ms.openlocfilehash: 3bedeb243b79cada713889145771d45511cb7b7f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776842"
---
# <span data-ttu-id="74508-101">Set-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="74508-101">Set-AzVMChefExtension</span></span>

## <span data-ttu-id="74508-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="74508-102">SYNOPSIS</span></span>
<span data-ttu-id="74508-103">Adiciona uma extensão chefe a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="74508-103">Adds a Chef extension to a virtual machine.</span></span>

## <span data-ttu-id="74508-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="74508-104">SYNTAX</span></span>

### <span data-ttu-id="74508-105">Linux</span><span class="sxs-lookup"><span data-stu-id="74508-105">Linux</span></span>
```
Set-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-TypeHandlerVersion] <String>]
 -ValidationPem <String> [-ClientRb <String>] [-BootstrapOptions <String>] [-JsonAttribute <String>]
 [-ChefDaemonInterval <String>] [-Daemon <String>] [-Secret <String>] [-SecretFile <String>]
 [-RunList <String>] [-ChefServerUrl <String>] [-ValidationClientName <String>] [-OrganizationName <String>]
 [-BootstrapVersion <String>] [-Linux] [[-Location] <String>] [[-Name] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="74508-106">Windows</span><span class="sxs-lookup"><span data-stu-id="74508-106">Windows</span></span>
```
Set-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-TypeHandlerVersion] <String>]
 -ValidationPem <String> [-ClientRb <String>] [-BootstrapOptions <String>] [-JsonAttribute <String>]
 [-ChefDaemonInterval <String>] [-Daemon <String>] [-Secret <String>] [-SecretFile <String>]
 [-RunList <String>] [-ChefServerUrl <String>] [-ValidationClientName <String>] [-OrganizationName <String>]
 [-BootstrapVersion <String>] [-Windows] [[-Location] <String>] [[-Name] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="74508-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="74508-107">DESCRIPTION</span></span>
<span data-ttu-id="74508-108">O cmdlet **set-AzureVMChefExtension** adiciona a extensão chefe à máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="74508-108">The **Set-AzureVMChefExtension** cmdlet adds the Chef extension to the virtual machine.</span></span>

## <span data-ttu-id="74508-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="74508-109">EXAMPLES</span></span>

### <span data-ttu-id="74508-110">Exemplo 1: adicionar uma extensão chefe a um computador virtual do Windows</span><span class="sxs-lookup"><span data-stu-id="74508-110">Example 1: Add a Chef extension to a Windows virtual machine</span></span>
```
PS C:\> Set-AzVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -ValidationPem "C:\my-org-validator.pem" -ClientRb "C:\client.rb" -RunList "Apache" -Daemon "service" -SecretFile "C:\my_encrypted_data_bag_secret" -Windows
```

<span data-ttu-id="74508-111">Esse comando adiciona uma extensão chefe a um computador virtual do Windows chamado WindowsVM001.</span><span class="sxs-lookup"><span data-stu-id="74508-111">This command adds a Chef extension to a Windows virtual machine named WindowsVM001.</span></span>
<span data-ttu-id="74508-112">Quando a máquina virtual for iniciada, o chefe inicializará a máquina virtual para executar o Apache.</span><span class="sxs-lookup"><span data-stu-id="74508-112">When the virtual machine starts, Chef bootstraps the virtual machine to run Apache.</span></span>

### <span data-ttu-id="74508-113">Exemplo 2: adicionar uma extensão chefe a um computador virtual Linux</span><span class="sxs-lookup"><span data-stu-id="74508-113">Example 2: Add a Chef extension to a Linux virtual machine</span></span>
```
PS C:\> Set-AzVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -ValidationPem "C:\my-org-validator.pem" -ClientRb "C:\client.rb" -RunList "Apache" -Secret "my_secret" -Linux
```

<span data-ttu-id="74508-114">Esse comando adiciona uma extensão chefe a um computador virtual Linux chamado LinuxVM001.</span><span class="sxs-lookup"><span data-stu-id="74508-114">This command adds a Chef extension to a Linux virtual machine named LinuxVM001.</span></span>
<span data-ttu-id="74508-115">Quando a máquina virtual for iniciada, o chefe inicializará a máquina virtual para executar o Apache.</span><span class="sxs-lookup"><span data-stu-id="74508-115">When the virtual machine starts, Chef bootstraps the virtual machine to run Apache.</span></span>

### <span data-ttu-id="74508-116">Exemplo 3: adicionar uma extensão chefe a um computador virtual do Windows com opções de inicialização</span><span class="sxs-lookup"><span data-stu-id="74508-116">Example 3: Add a Chef extension to a Windows virtual machine with bootstrap options</span></span>
```
PS C:\> Set-AzVMChefExtension -ResourceGroupName "ResourceGroup003" -VMName "WindowsVM002" -ValidationPem C:\my-org-validator.pem -ClientRb C:\client.rb -BootstrapOptions '{"chef_node_name":"your_node_name","chef_server_url":"https://api.opscode.com/organizations/some-org", "validation_client_name":"some-org-validator"}' -RunList "Apache" -Windows
```

<span data-ttu-id="74508-117">Esse comando adiciona a extensão chefe a um computador virtual do Windows chamado WindowsVM002.</span><span class="sxs-lookup"><span data-stu-id="74508-117">This command adds the Chef extension to a Windows virtual machine named WindowsVM002.</span></span>
<span data-ttu-id="74508-118">Quando a máquina virtual for iniciada, o chefe inicializará a máquina virtual para executar o Apache.</span><span class="sxs-lookup"><span data-stu-id="74508-118">When the virtual machine starts, Chef bootstraps the virtual machine to run Apache.</span></span>
<span data-ttu-id="74508-119">Após a inicialização, a máquina virtual refere-se à Bootstrapoptions especificada no formato JSON.</span><span class="sxs-lookup"><span data-stu-id="74508-119">After bootstrapping, the virtual machine refers to the BootstrapOptions specified in JSON format.</span></span>

## <span data-ttu-id="74508-120">OS</span><span class="sxs-lookup"><span data-stu-id="74508-120">PARAMETERS</span></span>

### <span data-ttu-id="74508-121">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="74508-121">-AutoUpgradeMinorVersion</span></span>
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74508-122">-Bootstrapoptions</span><span class="sxs-lookup"><span data-stu-id="74508-122">-BootstrapOptions</span></span>
<span data-ttu-id="74508-123">Especifica as definições de configuração na opção client_rb.</span><span class="sxs-lookup"><span data-stu-id="74508-123">Specifies configuration settings in the client_rb option.</span></span>

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

### <span data-ttu-id="74508-124">-BootstrapVersion</span><span class="sxs-lookup"><span data-stu-id="74508-124">-BootstrapVersion</span></span>
<span data-ttu-id="74508-125">Especifica a versão da configuração de inicialização.</span><span class="sxs-lookup"><span data-stu-id="74508-125">Specifies the version of the bootstrap configuration.</span></span>

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

### <span data-ttu-id="74508-126">-ChefDaemonInterval</span><span class="sxs-lookup"><span data-stu-id="74508-126">-ChefDaemonInterval</span></span>
<span data-ttu-id="74508-127">Especifica a frequência (em minutos) em que o chefe-serviço é executado.</span><span class="sxs-lookup"><span data-stu-id="74508-127">Specifies the frequency (in minutes) at which the chef-service runs.</span></span> <span data-ttu-id="74508-128">Se, caso não queira que o chefe-serviço seja instalado na máquina virtual do Azure, defina o valor como 0 nesse campo.</span><span class="sxs-lookup"><span data-stu-id="74508-128">If in case you don't want the chef-service to be installed on the Azure VM then set value as 0 in this field.</span></span>

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

### <span data-ttu-id="74508-129">-ChefServerUrl</span><span class="sxs-lookup"><span data-stu-id="74508-129">-ChefServerUrl</span></span>
<span data-ttu-id="74508-130">Especifica o link do servidor chefe como uma URL.</span><span class="sxs-lookup"><span data-stu-id="74508-130">Specifies the Chef server link, as a URL.</span></span>

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

### <span data-ttu-id="74508-131">-ClientRb</span><span class="sxs-lookup"><span data-stu-id="74508-131">-ClientRb</span></span>
<span data-ttu-id="74508-132">Especifica o caminho completo do chefe cliente. rb.</span><span class="sxs-lookup"><span data-stu-id="74508-132">Specifies the full path of the Chef client.rb.</span></span>

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

### <span data-ttu-id="74508-133">-Daemon</span><span class="sxs-lookup"><span data-stu-id="74508-133">-Daemon</span></span>
<span data-ttu-id="74508-134">Configura o serviço chefe-cliente para execução automática.</span><span class="sxs-lookup"><span data-stu-id="74508-134">Configures the chef-client service for unattended execution.</span></span> <span data-ttu-id="74508-135">A plataforma do nó deve ser Windows.</span><span class="sxs-lookup"><span data-stu-id="74508-135">The node platform should be Windows.</span></span>
<span data-ttu-id="74508-136">Opções permitidas: ' none ', ' Service ' e ' Task '.</span><span class="sxs-lookup"><span data-stu-id="74508-136">Allowed options: 'none','service' and 'task'.</span></span>
<span data-ttu-id="74508-137">None-atualmente impede que o serviço chefe-cliente seja configurado como um serviço.</span><span class="sxs-lookup"><span data-stu-id="74508-137">none - Currently prevents the chef-client service from being configured as a service.</span></span>
<span data-ttu-id="74508-138">serviço-configura o chefe-cliente para ser executado automaticamente em segundo plano como um serviço.</span><span class="sxs-lookup"><span data-stu-id="74508-138">service - Configures the chef-client to run automatically in the background as a service.</span></span>
<span data-ttu-id="74508-139">Task-configura o chefe-cliente para ser executado automaticamente em segundo plano como uma tarefa secheduled.</span><span class="sxs-lookup"><span data-stu-id="74508-139">task - Configures the chef-client to run automatically in the background as a secheduled task.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: none, service, task

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74508-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74508-140">-DefaultProfile</span></span>
<span data-ttu-id="74508-141">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="74508-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74508-142">-Jsonattribute</span><span class="sxs-lookup"><span data-stu-id="74508-142">-JsonAttribute</span></span>
<span data-ttu-id="74508-143">Uma cadeia de caracteres JSON a ser adicionada à primeira execução do chefe-cliente.</span><span class="sxs-lookup"><span data-stu-id="74508-143">A JSON string to be added to the first run of chef-client.</span></span> <span data-ttu-id="74508-144">por exemplo:-Jsonattribute ' {"foo": "barra"} '</span><span class="sxs-lookup"><span data-stu-id="74508-144">e.g. -JsonAttribute '{"foo" : "bar"}'</span></span>

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

### <span data-ttu-id="74508-145">-Linux</span><span class="sxs-lookup"><span data-stu-id="74508-145">-Linux</span></span>
<span data-ttu-id="74508-146">Indica que esse cmdlet cria um computador virtual do Windows.</span><span class="sxs-lookup"><span data-stu-id="74508-146">Indicates that this cmdlet creates a Windows virtual machine.</span></span>

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

### <span data-ttu-id="74508-147">-Local</span><span class="sxs-lookup"><span data-stu-id="74508-147">-Location</span></span>
<span data-ttu-id="74508-148">Especifica o local da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="74508-148">Specifies the location of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74508-149">-Nome</span><span class="sxs-lookup"><span data-stu-id="74508-149">-Name</span></span>
<span data-ttu-id="74508-150">Especifica o nome da extensão do chefe.</span><span class="sxs-lookup"><span data-stu-id="74508-150">Specifies the name of the Chef extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74508-151">-OrganizationName</span><span class="sxs-lookup"><span data-stu-id="74508-151">-OrganizationName</span></span>
<span data-ttu-id="74508-152">Especifica o nome da organização da extensão chefe.</span><span class="sxs-lookup"><span data-stu-id="74508-152">Specifies the organization name of the Chef extension.</span></span>

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

### <span data-ttu-id="74508-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74508-153">-ResourceGroupName</span></span>
<span data-ttu-id="74508-154">Especifica o nome do grupo de recursos que contém a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="74508-154">Specifies the name of the resource group that contains the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74508-155">-RunList</span><span class="sxs-lookup"><span data-stu-id="74508-155">-RunList</span></span>
<span data-ttu-id="74508-156">Especifica a lista de execução do nó chefe.</span><span class="sxs-lookup"><span data-stu-id="74508-156">Specifies the Chef node run list.</span></span>

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

### <span data-ttu-id="74508-157">-Segredo</span><span class="sxs-lookup"><span data-stu-id="74508-157">-Secret</span></span>
<span data-ttu-id="74508-158">A chave de criptografia usada para criptografar e descriptografar os valores de item do conjunto de dados.</span><span class="sxs-lookup"><span data-stu-id="74508-158">The encryption key used to encrypt and decrypt the data bag item values.</span></span>

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

### <span data-ttu-id="74508-159">-Secretfile</span><span class="sxs-lookup"><span data-stu-id="74508-159">-SecretFile</span></span>
<span data-ttu-id="74508-160">O caminho para o arquivo que contém a chave de criptografia usada para criptografar e descriptografar os valores de item do conjunto de dados.</span><span class="sxs-lookup"><span data-stu-id="74508-160">The path to the file that contains the encryption key used to encrypt and decrypt the data bag item values.</span></span>

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

### <span data-ttu-id="74508-161">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="74508-161">-TypeHandlerVersion</span></span>
<span data-ttu-id="74508-162">Especifica a versão da extensão a ser usada para esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="74508-162">Specifies the version of the extension to use for this virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74508-163">-ValidationClientName</span><span class="sxs-lookup"><span data-stu-id="74508-163">-ValidationClientName</span></span>
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

### <span data-ttu-id="74508-164">-ValidationPem</span><span class="sxs-lookup"><span data-stu-id="74508-164">-ValidationPem</span></span>
<span data-ttu-id="74508-165">Especifica o caminho do arquivo. PEM do chefe Validator</span><span class="sxs-lookup"><span data-stu-id="74508-165">Specifies the Chef validator .pem file path</span></span>

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

### <span data-ttu-id="74508-166">-VMName</span><span class="sxs-lookup"><span data-stu-id="74508-166">-VMName</span></span>
<span data-ttu-id="74508-167">Especifica o nome de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="74508-167">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="74508-168">Esse cmdlet adiciona a extensão chefe para a máquina virtual que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="74508-168">This cmdlet adds the Chef extension for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74508-169">-Windows</span><span class="sxs-lookup"><span data-stu-id="74508-169">-Windows</span></span>
<span data-ttu-id="74508-170">Indica que esse cmdlet cria um computador virtual do Windows.</span><span class="sxs-lookup"><span data-stu-id="74508-170">Indicates that this cmdlet creates a Windows virtual machine.</span></span>

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

### <span data-ttu-id="74508-171">-Confirme</span><span class="sxs-lookup"><span data-stu-id="74508-171">-Confirm</span></span>
<span data-ttu-id="74508-172">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74508-172">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74508-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74508-173">-WhatIf</span></span>
<span data-ttu-id="74508-174">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="74508-174">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="74508-175">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="74508-175">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74508-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74508-176">CommonParameters</span></span>
<span data-ttu-id="74508-177">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74508-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74508-178">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74508-178">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74508-179">SENSORES</span><span class="sxs-lookup"><span data-stu-id="74508-179">INPUTS</span></span>

### <span data-ttu-id="74508-180">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="74508-180">None</span></span>
<span data-ttu-id="74508-181">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="74508-181">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="74508-182">EXIBE</span><span class="sxs-lookup"><span data-stu-id="74508-182">OUTPUTS</span></span>

### <span data-ttu-id="74508-183">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="74508-183">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="74508-184">INFORMA</span><span class="sxs-lookup"><span data-stu-id="74508-184">NOTES</span></span>

## <span data-ttu-id="74508-185">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="74508-185">RELATED LINKS</span></span>

[<span data-ttu-id="74508-186">Get-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="74508-186">Get-AzVMChefExtension</span></span>](./Get-AzVMChefExtension.md)

[<span data-ttu-id="74508-187">Remove-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="74508-187">Remove-AzVMChefExtension</span></span>](./Remove-AzVMChefExtension.md)
