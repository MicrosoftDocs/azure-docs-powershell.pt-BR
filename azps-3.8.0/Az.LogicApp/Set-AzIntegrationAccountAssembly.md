---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountassembly
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountAssembly.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountAssembly.md
ms.openlocfilehash: 44f44fab1cbdd5346bbda4e1271c8dbf33b0e9f2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93940436"
---
# <span data-ttu-id="a01c1-101">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="a01c1-101">Set-AzIntegrationAccountAssembly</span></span>

## <span data-ttu-id="a01c1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a01c1-102">SYNOPSIS</span></span>
<span data-ttu-id="a01c1-103">Modifica um assembly da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="a01c1-103">Modifies an integration account assembly.</span></span>

## <span data-ttu-id="a01c1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a01c1-104">SYNTAX</span></span>

### <span data-ttu-id="a01c1-105">ByIntegrationAccountAndFilePath (padrão)</span><span class="sxs-lookup"><span data-stu-id="a01c1-105">ByIntegrationAccountAndFilePath (Default)</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -AssemblyFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a01c1-106">ByIntegrationAccountAndContentLink</span><span class="sxs-lookup"><span data-stu-id="a01c1-106">ByIntegrationAccountAndContentLink</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -ContentLink <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a01c1-107">ByIntegrationAccountAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="a01c1-107">ByIntegrationAccountAndFileBytes</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -AssemblyData <Byte[]> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a01c1-108">ByInputObjectAndContentLink</span><span class="sxs-lookup"><span data-stu-id="a01c1-108">ByInputObjectAndContentLink</span></span>
```
Set-AzIntegrationAccountAssembly -InputObject <PSIntegrationAccountAssembly> -ContentLink <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a01c1-109">ByInputObjectAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="a01c1-109">ByInputObjectAndFileBytes</span></span>
```
Set-AzIntegrationAccountAssembly -InputObject <PSIntegrationAccountAssembly> -AssemblyData <Byte[]>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a01c1-110">ByInputObjectAndFilePath</span><span class="sxs-lookup"><span data-stu-id="a01c1-110">ByInputObjectAndFilePath</span></span>
```
Set-AzIntegrationAccountAssembly -InputObject <PSIntegrationAccountAssembly> -AssemblyFilePath <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a01c1-111">ByResourceIdAndContentLink</span><span class="sxs-lookup"><span data-stu-id="a01c1-111">ByResourceIdAndContentLink</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceId <String> -ContentLink <String> [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a01c1-112">ByResourceIdAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="a01c1-112">ByResourceIdAndFileBytes</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceId <String> -AssemblyData <Byte[]> [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a01c1-113">ByResourceIdAndFilePath</span><span class="sxs-lookup"><span data-stu-id="a01c1-113">ByResourceIdAndFilePath</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceId <String> -AssemblyFilePath <String> [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a01c1-114">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a01c1-114">DESCRIPTION</span></span>
<span data-ttu-id="a01c1-115">O cmdlet **set-AzIntegrationAccountAssembly** modifica um assembly de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="a01c1-115">The **Set-AzIntegrationAccountAssembly** cmdlet modifies an integration account assembly.</span></span>

## <span data-ttu-id="a01c1-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a01c1-116">EXAMPLES</span></span>

### <span data-ttu-id="a01c1-117">Exemplo 1: modificar um assembly usando um arquivo local</span><span class="sxs-lookup"><span data-stu-id="a01c1-117">Example 1: Modify an assembly using local file</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -AssemblyFilePath $localAssemblyFilePath

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="a01c1-118">Modifica o assembly chamado "sampleAssembly" usando o arquivo local localizado no caminho do arquivo contido em "$localAssemblyFilePath".</span><span class="sxs-lookup"><span data-stu-id="a01c1-118">Modifies the assembly named "sampleAssembly" using the local file located at the file path contained in "$localAssemblyFilePath".</span></span>

### <span data-ttu-id="a01c1-119">Exemplo 2: modificar um assembly usando dados de bytes</span><span class="sxs-lookup"><span data-stu-id="a01c1-119">Example 2: Modify an assembly using byte data</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -AssemblyData $assemblyContent

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="a01c1-120">Modifica o assembly chamado "sampleAssembly" usando a matriz de bytes contida em "$assemblyContent".</span><span class="sxs-lookup"><span data-stu-id="a01c1-120">Modifies the assembly named "sampleAssembly" using the a byte array contained in "$assemblyContent".</span></span>

### <span data-ttu-id="a01c1-121">Exemplo 3: modificar um assembly usando um link de conteúdo</span><span class="sxs-lookup"><span data-stu-id="a01c1-121">Example 3: Modify an assembly using a content link</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -ContentLink $assemblyUrl

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="a01c1-122">Modifica o assembly chamado "sampleAssembly" usando os dados de bytes localizados na URL "$assemblyUrl".</span><span class="sxs-lookup"><span data-stu-id="a01c1-122">Modifies the assembly named "sampleAssembly" using the a byte data located at the URL "$assemblyUrl".</span></span> <span data-ttu-id="a01c1-123">Esse é o método sugerido para a criação de conjuntos de grandes tamanhos.</span><span class="sxs-lookup"><span data-stu-id="a01c1-123">This is the suggested method for creating large sized assemblies.</span></span>

## <span data-ttu-id="a01c1-124">OS</span><span class="sxs-lookup"><span data-stu-id="a01c1-124">PARAMETERS</span></span>

### <span data-ttu-id="a01c1-125">-AssemblyData</span><span class="sxs-lookup"><span data-stu-id="a01c1-125">-AssemblyData</span></span>
<span data-ttu-id="a01c1-126">A conta de integração assembly dados de bytes.</span><span class="sxs-lookup"><span data-stu-id="a01c1-126">The integration account assembly byte data.</span></span>

```yaml
Type: System.Byte[]
Parameter Sets: ByIntegrationAccountAndFileBytes, ByInputObjectAndFileBytes, ByResourceIdAndFileBytes
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a01c1-127">-AssemblyFilePath</span><span class="sxs-lookup"><span data-stu-id="a01c1-127">-AssemblyFilePath</span></span>
<span data-ttu-id="a01c1-128">O caminho do arquivo de assembly da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="a01c1-128">The integration account assembly file path.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndFilePath, ByInputObjectAndFilePath, ByResourceIdAndFilePath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a01c1-129">-ContentLink</span><span class="sxs-lookup"><span data-stu-id="a01c1-129">-ContentLink</span></span>
<span data-ttu-id="a01c1-130">Um link publicamente acessível para os dados de assembly da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="a01c1-130">A publicly accessible link to the integration account assembly data.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndContentLink, ByInputObjectAndContentLink, ByResourceIdAndContentLink
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a01c1-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a01c1-131">-DefaultProfile</span></span>
<span data-ttu-id="a01c1-132">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a01c1-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a01c1-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a01c1-133">-InputObject</span></span>
<span data-ttu-id="a01c1-134">Um assembly de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="a01c1-134">An integration account assembly.</span></span>

```yaml
Type: Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly
Parameter Sets: ByInputObjectAndContentLink, ByInputObjectAndFileBytes, ByInputObjectAndFilePath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a01c1-135">-Metadados</span><span class="sxs-lookup"><span data-stu-id="a01c1-135">-Metadata</span></span>
<span data-ttu-id="a01c1-136">Os metadados de assembly da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="a01c1-136">The integration account assembly metadata.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a01c1-137">-Nome</span><span class="sxs-lookup"><span data-stu-id="a01c1-137">-Name</span></span>
<span data-ttu-id="a01c1-138">O nome do assembly da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="a01c1-138">The integration account assembly name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndFilePath, ByIntegrationAccountAndContentLink, ByIntegrationAccountAndFileBytes
Aliases: AssemblyName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a01c1-139">-ParentName</span><span class="sxs-lookup"><span data-stu-id="a01c1-139">-ParentName</span></span>
<span data-ttu-id="a01c1-140">O nome da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="a01c1-140">The integration account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndFilePath, ByIntegrationAccountAndContentLink, ByIntegrationAccountAndFileBytes
Aliases: IntegrationAccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a01c1-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a01c1-141">-ResourceGroupName</span></span>
<span data-ttu-id="a01c1-142">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a01c1-142">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndFilePath, ByIntegrationAccountAndContentLink, ByIntegrationAccountAndFileBytes
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a01c1-143">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a01c1-143">-ResourceId</span></span>
<span data-ttu-id="a01c1-144">A ID do recurso assembly da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="a01c1-144">The integration account assembly resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdAndContentLink, ByResourceIdAndFileBytes, ByResourceIdAndFilePath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a01c1-145">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a01c1-145">-Confirm</span></span>
<span data-ttu-id="a01c1-146">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a01c1-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a01c1-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a01c1-147">-WhatIf</span></span>
<span data-ttu-id="a01c1-148">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a01c1-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a01c1-149">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a01c1-149">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a01c1-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a01c1-150">CommonParameters</span></span>
<span data-ttu-id="a01c1-151">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a01c1-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a01c1-152">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a01c1-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a01c1-153">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a01c1-153">INPUTS</span></span>

### <span data-ttu-id="a01c1-154">Microsoft. Azure. Commands. LogicApp. Models. PSIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="a01c1-154">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

### <span data-ttu-id="a01c1-155">System. String</span><span class="sxs-lookup"><span data-stu-id="a01c1-155">System.String</span></span>

## <span data-ttu-id="a01c1-156">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a01c1-156">OUTPUTS</span></span>

### <span data-ttu-id="a01c1-157">Microsoft. Azure. Commands. LogicApp. Models. PSIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="a01c1-157">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

## <span data-ttu-id="a01c1-158">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a01c1-158">NOTES</span></span>

## <span data-ttu-id="a01c1-159">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a01c1-159">RELATED LINKS</span></span>
