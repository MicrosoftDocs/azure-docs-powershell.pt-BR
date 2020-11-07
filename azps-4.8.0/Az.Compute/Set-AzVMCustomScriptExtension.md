---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 64AB1BAE-A756-43A8-A40F-10B746EA0946
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmcustomscriptextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMCustomScriptExtension.md
ms.openlocfilehash: 69b6dec11f0135803320bb7b58bdb8362aaee26e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93948396"
---
# <span data-ttu-id="046bf-101">Set-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="046bf-101">Set-AzVMCustomScriptExtension</span></span>

## <span data-ttu-id="046bf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="046bf-102">SYNOPSIS</span></span>
<span data-ttu-id="046bf-103">Adiciona uma extensão de script personalizada a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="046bf-103">Adds a custom script extension to a virtual machine.</span></span>

## <span data-ttu-id="046bf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="046bf-104">SYNTAX</span></span>

### <span data-ttu-id="046bf-105">ByNameWithContainerAndFileNamesParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="046bf-105">ByNameWithContainerAndFileNamesParameterSet (Default)</span></span>
```
Set-AzVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 -ContainerName <String> -FileName <String[]> [-StorageAccountName <String>] [-StorageEndpointSuffix <String>]
 [-StorageAccountKey <String>] [-Run <String>] [-Argument <String>] [-SecureExecution]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="046bf-106">ByNameWithFileUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="046bf-106">ByNameWithFileUriParameterSet</span></span>
```
Set-AzVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-FileUri <String[]>] [-Run <String>] [-Argument <String>] [-SecureExecution] [-TypeHandlerVersion <String>]
 [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="046bf-107">ByParentObjectWithContainerAndFileNamesParameterSet</span><span class="sxs-lookup"><span data-stu-id="046bf-107">ByParentObjectWithContainerAndFileNamesParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -Name <String> -VMObject <PSVirtualMachine> -ContainerName <String>
 -FileName <String[]> [-StorageAccountName <String>] [-StorageEndpointSuffix <String>]
 [-StorageAccountKey <String>] [-Run <String>] [-Argument <String>] [-SecureExecution]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="046bf-108">ByParentObjectWithFileUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="046bf-108">ByParentObjectWithFileUriParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -Name <String> -VMObject <PSVirtualMachine> [-FileUri <String[]>] [-Run <String>]
 [-Argument <String>] [-SecureExecution] [-TypeHandlerVersion <String>] [-Location <String>]
 [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="046bf-109">ByResourceIdWithContainerAndFileNamesParameterSet</span><span class="sxs-lookup"><span data-stu-id="046bf-109">ByResourceIdWithContainerAndFileNamesParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -ResourceId <String> -ContainerName <String> -FileName <String[]>
 [-StorageAccountName <String>] [-StorageEndpointSuffix <String>] [-StorageAccountKey <String>] [-Run <String>]
 [-Argument <String>] [-SecureExecution] [-TypeHandlerVersion <String>] [-Location <String>]
 [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="046bf-110">ByResourceIdWithFileUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="046bf-110">ByResourceIdWithFileUriParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -ResourceId <String> [-FileUri <String[]>] [-Run <String>] [-Argument <String>]
 [-SecureExecution] [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion]
 [-ForceRerun <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="046bf-111">ByInputObjectWithContainerAndFileNamesParameterSet</span><span class="sxs-lookup"><span data-stu-id="046bf-111">ByInputObjectWithContainerAndFileNamesParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -InputObject <VirtualMachineCustomScriptExtensionContext> -ContainerName <String>
 -FileName <String[]> [-StorageAccountName <String>] [-StorageEndpointSuffix <String>]
 [-StorageAccountKey <String>] [-Run <String>] [-Argument <String>] [-SecureExecution]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="046bf-112">ByInputObjectWithFileUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="046bf-112">ByInputObjectWithFileUriParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -InputObject <VirtualMachineCustomScriptExtensionContext> [-FileUri <String[]>]
 [-Run <String>] [-Argument <String>] [-SecureExecution] [-TypeHandlerVersion <String>] [-Location <String>]
 [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="046bf-113">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="046bf-113">DESCRIPTION</span></span>
<span data-ttu-id="046bf-114">O cmdlet **set-AzVMCustomScriptExtension** adiciona uma extensão de máquina virtual de script personalizado a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="046bf-114">The **Set-AzVMCustomScriptExtension** cmdlet adds a custom script Virtual Machine Extension to a virtual machine.</span></span>
<span data-ttu-id="046bf-115">Essa extensão permite que você execute seus próprios scripts na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="046bf-115">This extension lets you run your own scripts on the virtual machine.</span></span>

## <span data-ttu-id="046bf-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="046bf-116">EXAMPLES</span></span>

### <span data-ttu-id="046bf-117">Exemplo 1: adicionar um script personalizado</span><span class="sxs-lookup"><span data-stu-id="046bf-117">Example 1: Add a custom script</span></span>
```powershell
PS C:\> Set-AzVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -Location "Central US" -VMName "VirtualMachine07" -Name "ContosoTest" -TypeHandlerVersion "1.1" -StorageAccountName "Contoso" -StorageAccountKey <StorageKey> -FileName "ContosoScript.exe" -ContainerName "Scripts"
```

<span data-ttu-id="046bf-118">Esse comando adiciona um script personalizado à máquina virtual chamada VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="046bf-118">This command adds a custom script to the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="046bf-119">O arquivo de script é contososcript.exe.</span><span class="sxs-lookup"><span data-stu-id="046bf-119">The script file is contososcript.exe.</span></span>

### <span data-ttu-id="046bf-120">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="046bf-120">Example 2</span></span>

<span data-ttu-id="046bf-121">Adiciona uma extensão de script personalizada a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="046bf-121">Adds a custom script extension to a virtual machine.</span></span> <span data-ttu-id="046bf-122">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="046bf-122">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzVMCustomScriptExtension -Argument <String> -ContainerName 'Scripts' -DefaultProfile <IAzureContextContainer> -FileName 'ContosoScript.exe' -Location 'Central US' -Name 'ContosoTest' -ResourceGroupName 'ResourceGroup11' -Run 'myScript.ps1' -SecureExecution -StorageAccountKey <String> -StorageAccountName 'Contoso' -TypeHandlerVersion '1.1' -VMName 'VirtualMachine07'
```

## <span data-ttu-id="046bf-123">OS</span><span class="sxs-lookup"><span data-stu-id="046bf-123">PARAMETERS</span></span>

### <span data-ttu-id="046bf-124">-Argumento</span><span class="sxs-lookup"><span data-stu-id="046bf-124">-Argument</span></span>
<span data-ttu-id="046bf-125">Especifica os argumentos que a extensão de script passa para o script.</span><span class="sxs-lookup"><span data-stu-id="046bf-125">Specifies arguments that the script extension passes to the script.</span></span>

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

### <span data-ttu-id="046bf-126">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="046bf-126">-ContainerName</span></span>
<span data-ttu-id="046bf-127">Especifica o nome do contêiner de armazenamento do Azure em que esse cmdlet armazena o script.</span><span class="sxs-lookup"><span data-stu-id="046bf-127">Specifies the name of the Azure storage container where this cmdlet stores the script.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameWithContainerAndFileNamesParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByParentObjectWithContainerAndFileNamesParameterSet, ByResourceIdWithContainerAndFileNamesParameterSet, ByInputObjectWithContainerAndFileNamesParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="046bf-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="046bf-128">-DefaultProfile</span></span>
<span data-ttu-id="046bf-129">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="046bf-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="046bf-130">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="046bf-130">-DisableAutoUpgradeMinorVersion</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="046bf-131">-Nome do arquivo</span><span class="sxs-lookup"><span data-stu-id="046bf-131">-FileName</span></span>
<span data-ttu-id="046bf-132">Especifica o nome do arquivo de script.</span><span class="sxs-lookup"><span data-stu-id="046bf-132">Specifies the name of the script file.</span></span> <span data-ttu-id="046bf-133">Se o arquivo estiver armazenado no armazenamento do blob do Azure, o valor do nome do arquivo diferenciará maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="046bf-133">If the file is stored in Azure Blob storage, the file name value is case-sensitive.</span></span> <span data-ttu-id="046bf-134">Os nomes de arquivo dos arquivos armazenados no armazenamento de arquivos do Azure não diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="046bf-134">File names of files stored in Azure File storage are not case-sensitive.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByNameWithContainerAndFileNamesParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: ByParentObjectWithContainerAndFileNamesParameterSet, ByResourceIdWithContainerAndFileNamesParameterSet, ByInputObjectWithContainerAndFileNamesParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="046bf-135">-FileUri</span><span class="sxs-lookup"><span data-stu-id="046bf-135">-FileUri</span></span>
<span data-ttu-id="046bf-136">Especifica o URI do arquivo de script.</span><span class="sxs-lookup"><span data-stu-id="046bf-136">Specifies the URI of the script file.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByNameWithFileUriParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: ByParentObjectWithFileUriParameterSet, ByResourceIdWithFileUriParameterSet, ByInputObjectWithFileUriParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="046bf-137">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="046bf-137">-ForceRerun</span></span>
<span data-ttu-id="046bf-138">Indica que esse cmdlet força uma nova configuração da mesma extensão na máquina virtual sem desinstalar e reinstalar a extensão.</span><span class="sxs-lookup"><span data-stu-id="046bf-138">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="046bf-139">O valor pode ser qualquer cadeia de caracteres diferente do valor atual.</span><span class="sxs-lookup"><span data-stu-id="046bf-139">The value can be any string different from the current value.</span></span>
<span data-ttu-id="046bf-140">Se forceUpdateTag não for alterado, as atualizações para as configurações públicas ou protegidas ainda serão aplicadas pelo manipulador.</span><span class="sxs-lookup"><span data-stu-id="046bf-140">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="046bf-141">-InputObject</span><span class="sxs-lookup"><span data-stu-id="046bf-141">-InputObject</span></span>
<span data-ttu-id="046bf-142">Objeto de extensão de VM.</span><span class="sxs-lookup"><span data-stu-id="046bf-142">VM extension object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.VirtualMachineCustomScriptExtensionContext
Parameter Sets: ByInputObjectWithContainerAndFileNamesParameterSet, ByInputObjectWithFileUriParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="046bf-143">-Local</span><span class="sxs-lookup"><span data-stu-id="046bf-143">-Location</span></span>
<span data-ttu-id="046bf-144">Especifica o local da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="046bf-144">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="046bf-145">-Nome</span><span class="sxs-lookup"><span data-stu-id="046bf-145">-Name</span></span>
<span data-ttu-id="046bf-146">Especifica o nome da extensão de script personalizada.</span><span class="sxs-lookup"><span data-stu-id="046bf-146">Specifies the name of the custom script extension.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameWithContainerAndFileNamesParameterSet, ByNameWithFileUriParameterSet
Aliases: ExtensionName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByParentObjectWithContainerAndFileNamesParameterSet, ByParentObjectWithFileUriParameterSet
Aliases: ExtensionName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="046bf-147">-Nowait</span><span class="sxs-lookup"><span data-stu-id="046bf-147">-NoWait</span></span>
<span data-ttu-id="046bf-148">Inicia a operação e retorna imediatamente, antes que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="046bf-148">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="046bf-149">Para determinar se a operação foi concluída com êxito, use outro mecanismo.</span><span class="sxs-lookup"><span data-stu-id="046bf-149">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="046bf-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="046bf-150">-ResourceGroupName</span></span>
<span data-ttu-id="046bf-151">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="046bf-151">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameWithContainerAndFileNamesParameterSet, ByNameWithFileUriParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="046bf-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="046bf-152">-ResourceId</span></span>
<span data-ttu-id="046bf-153">ResourceId da extensão da VM.</span><span class="sxs-lookup"><span data-stu-id="046bf-153">VM extension ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdWithContainerAndFileNamesParameterSet, ByResourceIdWithFileUriParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="046bf-154">-Executar</span><span class="sxs-lookup"><span data-stu-id="046bf-154">-Run</span></span>
<span data-ttu-id="046bf-155">Especifica o comando a ser usado para executar o script.</span><span class="sxs-lookup"><span data-stu-id="046bf-155">Specifies the command to use that runs your script.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RunFile, Command

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="046bf-156">-SecureExecution</span><span class="sxs-lookup"><span data-stu-id="046bf-156">-SecureExecution</span></span>
<span data-ttu-id="046bf-157">Indica que esse cmdlet garante que o valor do parâmetro de *execução* não esteja conectado ao servidor ou retornado ao usuário usando a API de extensão Get.</span><span class="sxs-lookup"><span data-stu-id="046bf-157">Indicates that this cmdlet makes sure that the value of the *Run* parameter is not logged on the server or returned to the user by using the GET extension API.</span></span>
<span data-ttu-id="046bf-158">O valor de *Run* pode conter segredos ou senhas a serem passados para o arquivo de script com segurança.</span><span class="sxs-lookup"><span data-stu-id="046bf-158">The value of *Run* might contain secrets or passwords to be passed to the script file securely.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="046bf-159">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="046bf-159">-StorageAccountKey</span></span>
<span data-ttu-id="046bf-160">Especifica a chave para o contêiner de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="046bf-160">Specifies the key for the Azure storage container.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameWithContainerAndFileNamesParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByParentObjectWithContainerAndFileNamesParameterSet, ByResourceIdWithContainerAndFileNamesParameterSet, ByInputObjectWithContainerAndFileNamesParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="046bf-161">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="046bf-161">-StorageAccountName</span></span>
<span data-ttu-id="046bf-162">Especifica o nome da conta de armazenamento do Azure na qual esse cmdlet armazena o script.</span><span class="sxs-lookup"><span data-stu-id="046bf-162">Specifies the name of the Azure storage account where this cmdlet stores the script.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameWithContainerAndFileNamesParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByParentObjectWithContainerAndFileNamesParameterSet, ByResourceIdWithContainerAndFileNamesParameterSet, ByInputObjectWithContainerAndFileNamesParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="046bf-163">-StorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="046bf-163">-StorageEndpointSuffix</span></span>
<span data-ttu-id="046bf-164">Especifica o sufixo de ponto de extremidade de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="046bf-164">Specifies the storage endpoint suffix.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameWithContainerAndFileNamesParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByParentObjectWithContainerAndFileNamesParameterSet, ByResourceIdWithContainerAndFileNamesParameterSet, ByInputObjectWithContainerAndFileNamesParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="046bf-165">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="046bf-165">-TypeHandlerVersion</span></span>
<span data-ttu-id="046bf-166">Especifica a versão da extensão a ser usada para esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="046bf-166">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="046bf-167">Para obter a versão, execute o cmdlet Get-AzVMExtensionImage com um valor de Microsoft. COMPUTE para o parâmetro *PublisherName* e CustomScriptExtension para o parâmetro de *tipo* .</span><span class="sxs-lookup"><span data-stu-id="046bf-167">To obtain the version, run the Get-AzVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and CustomScriptExtension for the *Type* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="046bf-168">-VMName</span><span class="sxs-lookup"><span data-stu-id="046bf-168">-VMName</span></span>
<span data-ttu-id="046bf-169">Especifica o nome de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="046bf-169">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="046bf-170">Esse cmdlet adiciona a extensão de script personalizada para a máquina virtual que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="046bf-170">This cmdlet adds the custom script extension for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameWithContainerAndFileNamesParameterSet, ByNameWithFileUriParameterSet
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="046bf-171">-VMObject</span><span class="sxs-lookup"><span data-stu-id="046bf-171">-VMObject</span></span>
<span data-ttu-id="046bf-172">Objeto VM.</span><span class="sxs-lookup"><span data-stu-id="046bf-172">VM object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: ByParentObjectWithContainerAndFileNamesParameterSet, ByParentObjectWithFileUriParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="046bf-173">-Confirme</span><span class="sxs-lookup"><span data-stu-id="046bf-173">-Confirm</span></span>
<span data-ttu-id="046bf-174">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="046bf-174">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="046bf-175">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="046bf-175">-WhatIf</span></span>
<span data-ttu-id="046bf-176">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="046bf-176">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="046bf-177">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="046bf-177">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="046bf-178">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="046bf-178">CommonParameters</span></span>
<span data-ttu-id="046bf-179">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="046bf-179">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="046bf-180">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="046bf-180">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="046bf-181">SENSORES</span><span class="sxs-lookup"><span data-stu-id="046bf-181">INPUTS</span></span>

### <span data-ttu-id="046bf-182">System. String</span><span class="sxs-lookup"><span data-stu-id="046bf-182">System.String</span></span>

### <span data-ttu-id="046bf-183">System. String []</span><span class="sxs-lookup"><span data-stu-id="046bf-183">System.String[]</span></span>

### <span data-ttu-id="046bf-184">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="046bf-184">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="046bf-185">EXIBE</span><span class="sxs-lookup"><span data-stu-id="046bf-185">OUTPUTS</span></span>

### <span data-ttu-id="046bf-186">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="046bf-186">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="046bf-187">INFORMA</span><span class="sxs-lookup"><span data-stu-id="046bf-187">NOTES</span></span>

## <span data-ttu-id="046bf-188">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="046bf-188">RELATED LINKS</span></span>

[<span data-ttu-id="046bf-189">Get-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="046bf-189">Get-AzVMCustomScriptExtension</span></span>](./Get-AzVMCustomScriptExtension.md)

[<span data-ttu-id="046bf-190">Remove-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="046bf-190">Remove-AzVMCustomScriptExtension</span></span>](./Remove-AzVMCustomScriptExtension.md)


