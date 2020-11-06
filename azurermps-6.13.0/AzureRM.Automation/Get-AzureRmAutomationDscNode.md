---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 6493186F-064B-45B7-8DFD-7799B1F2E5C9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNode.md
ms.openlocfilehash: a902c88c53736f1e0db238cdb53ea381e5e887a8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426466"
---
# <span data-ttu-id="0928e-101">Get-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="0928e-101">Get-AzureRmAutomationDscNode</span></span>

## <span data-ttu-id="0928e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0928e-102">SYNOPSIS</span></span>
<span data-ttu-id="0928e-103">Obtém nós DSC da automação.</span><span class="sxs-lookup"><span data-stu-id="0928e-103">Gets DSC nodes from Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0928e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0928e-104">SYNTAX</span></span>

### <span data-ttu-id="0928e-105">ByAll (padrão)</span><span class="sxs-lookup"><span data-stu-id="0928e-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationDscNode [-Status <DscNodeStatus>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0928e-106">ById</span><span class="sxs-lookup"><span data-stu-id="0928e-106">ById</span></span>
```
Get-AzureRmAutomationDscNode -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0928e-107">ByName</span><span class="sxs-lookup"><span data-stu-id="0928e-107">ByName</span></span>
```
Get-AzureRmAutomationDscNode [-Status <DscNodeStatus>] -Name <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0928e-108">ByNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="0928e-108">ByNodeConfiguration</span></span>
```
Get-AzureRmAutomationDscNode [-Status <DscNodeStatus>] -NodeConfigurationName <String>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0928e-109">ByConfiguration</span><span class="sxs-lookup"><span data-stu-id="0928e-109">ByConfiguration</span></span>
```
Get-AzureRmAutomationDscNode -ConfigurationName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0928e-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0928e-110">DESCRIPTION</span></span>
<span data-ttu-id="0928e-111">O cmdlet **Get-AzureRmAutomationDscNode** Obtém os nós DSC (configuração de estado desejado APS) da automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="0928e-111">The **Get-AzureRmAutomationDscNode** cmdlet gets APS Desired State Configuration (DSC) nodes from Azure Automation.</span></span>

## <span data-ttu-id="0928e-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0928e-112">EXAMPLES</span></span>

### <span data-ttu-id="0928e-113">Exemplo 1: obter todos os nós DSC</span><span class="sxs-lookup"><span data-stu-id="0928e-113">Example 1: Get all DSC nodes</span></span>
```
PS C:\>Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="0928e-114">Esse comando obtém metadados para todos os nós DSC na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="0928e-114">This command gets metadata for all DSC nodes in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="0928e-115">Exemplo 2: obter todos os nós DSC para uma configuração DSC</span><span class="sxs-lookup"><span data-stu-id="0928e-115">Example 2: Get all DSC nodes for a DSC configuration</span></span>
```
PS C:\>Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ConfigurationName "ContosoConfiguration"
```

<span data-ttu-id="0928e-116">Esse comando obtém metadados para todos os nós DSC da conta de automação chamados Contoso17 que são mapeados para uma configuração de nó DSC que foi gerada pelo ContosoConfiguration de configuração DSC.</span><span class="sxs-lookup"><span data-stu-id="0928e-116">This command gets metadata for all DSC nodes in the Automation account named Contoso17 that are mapped to a DSC node configuration which was generated by DSC configuration ContosoConfiguration.</span></span>

### <span data-ttu-id="0928e-117">Exemplo 3: obter um nó DSC por ID</span><span class="sxs-lookup"><span data-stu-id="0928e-117">Example 3: Get a DSC node by ID</span></span>
```
PS C:\>Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

<span data-ttu-id="0928e-118">Esse comando obtém metadados em um nó DSC com a ID especificada na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="0928e-118">This command gets metadata on a DSC node with the specified ID in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="0928e-119">Exemplo 4: obter um nó DSC por nome</span><span class="sxs-lookup"><span data-stu-id="0928e-119">Example 4: Get a DSC node by name</span></span>
```
PS C:\>Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
```

<span data-ttu-id="0928e-120">Esse comando obtém metadados em um nó DSC com o nome Computer14 na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="0928e-120">This command gets metadata on a DSC node with the name Computer14 in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="0928e-121">Exemplo 5: obter todos os nós DSC mapeados para uma configuração de nó DSC</span><span class="sxs-lookup"><span data-stu-id="0928e-121">Example 5: Get all DSC nodes mapped to a DSC node configuration</span></span>
```
PS C:\>Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeConfigurationName "ContosoConfiguration.webserver"
```

<span data-ttu-id="0928e-122">Esse comando obtém metadados sobre todos os nós DSC da conta de automação chamados Contoso17 que são mapeados para uma configuração de nó DSC nomeada ContosoConfiguration. WebServer.</span><span class="sxs-lookup"><span data-stu-id="0928e-122">This command gets metadata on all DSC nodes in the Automation account named Contoso17 that are mapped to a DSC node configuration named ContosoConfiguration.webserver.</span></span>

## <span data-ttu-id="0928e-123">OS</span><span class="sxs-lookup"><span data-stu-id="0928e-123">PARAMETERS</span></span>

### <span data-ttu-id="0928e-124">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="0928e-124">-AutomationAccountName</span></span>
<span data-ttu-id="0928e-125">Especifica o nome da conta de automação que contém os nós DSC que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="0928e-125">Specifies the name of the Automation account that contains the DSC nodes that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0928e-126">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="0928e-126">-ConfigurationName</span></span>
<span data-ttu-id="0928e-127">Especifica o nome de uma configuração DSC.</span><span class="sxs-lookup"><span data-stu-id="0928e-127">Specifies the name of a DSC configuration.</span></span>
<span data-ttu-id="0928e-128">Esse cmdlet obtém nós DSC que correspondem às configurações de nó geradas pela configuração que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="0928e-128">This cmdlet gets DSC nodes that match the node configurations generated from the configuration that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0928e-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0928e-129">-DefaultProfile</span></span>
<span data-ttu-id="0928e-130">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="0928e-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0928e-131">-ID</span><span class="sxs-lookup"><span data-stu-id="0928e-131">-Id</span></span>
<span data-ttu-id="0928e-132">Especifica a ID exclusiva do nó DSC que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="0928e-132">Specifies the unique ID of the DSC node that this cmdlet gets.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ById
Aliases: NodeId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0928e-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="0928e-133">-Name</span></span>
<span data-ttu-id="0928e-134">Especifica o nome de um nó DSC que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="0928e-134">Specifies the name of a DSC node that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: NodeName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0928e-135">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="0928e-135">-NodeConfigurationName</span></span>
<span data-ttu-id="0928e-136">Especifica o nome de uma configuração de nó obtida por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0928e-136">Specifies the name of a node configuration that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNodeConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0928e-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0928e-137">-ResourceGroupName</span></span>
<span data-ttu-id="0928e-138">Especifica o nome de um grupo de recursos em que esse cmdlet obtém nós DSC.</span><span class="sxs-lookup"><span data-stu-id="0928e-138">Specifies the name of a resource group in which this cmdlet gets DSC nodes.</span></span>

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

### <span data-ttu-id="0928e-139">-Status</span><span class="sxs-lookup"><span data-stu-id="0928e-139">-Status</span></span>
<span data-ttu-id="0928e-140">Especifica o status dos nós DSC que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="0928e-140">Specifies the status of the DSC nodes that this cmdlet gets.</span></span>
<span data-ttu-id="0928e-141">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="0928e-141">Valid values are:</span></span> 
- <span data-ttu-id="0928e-142">CLS</span><span class="sxs-lookup"><span data-stu-id="0928e-142">Compliant</span></span> 
- <span data-ttu-id="0928e-143">Não compatível</span><span class="sxs-lookup"><span data-stu-id="0928e-143">NotCompliant</span></span>
- <span data-ttu-id="0928e-144">Conseguiu</span><span class="sxs-lookup"><span data-stu-id="0928e-144">Failed</span></span>
- <span data-ttu-id="0928e-145">Pending</span><span class="sxs-lookup"><span data-stu-id="0928e-145">Pending</span></span> 
- <span data-ttu-id="0928e-146">Recebi</span><span class="sxs-lookup"><span data-stu-id="0928e-146">Received</span></span>
- <span data-ttu-id="0928e-147">Respondendo</span><span class="sxs-lookup"><span data-stu-id="0928e-147">Unresponsive</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Common.DscNodeStatus
Parameter Sets: ByAll, ByName, ByNodeConfiguration
Aliases:
Accepted values: Compliant, NotCompliant, Failed, Pending, Received, Unresponsive

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0928e-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0928e-148">CommonParameters</span></span>
<span data-ttu-id="0928e-149">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0928e-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0928e-150">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0928e-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0928e-151">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0928e-151">INPUTS</span></span>

### <span data-ttu-id="0928e-152">System. GUID</span><span class="sxs-lookup"><span data-stu-id="0928e-152">System.Guid</span></span>

### <span data-ttu-id="0928e-153">System. String</span><span class="sxs-lookup"><span data-stu-id="0928e-153">System.String</span></span>

## <span data-ttu-id="0928e-154">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0928e-154">OUTPUTS</span></span>

### <span data-ttu-id="0928e-155">Microsoft. Azure. Commands. Automation. Model. DscNode</span><span class="sxs-lookup"><span data-stu-id="0928e-155">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="0928e-156">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0928e-156">NOTES</span></span>

## <span data-ttu-id="0928e-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0928e-157">RELATED LINKS</span></span>

[<span data-ttu-id="0928e-158">Register-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="0928e-158">Register-AzureRmAutomationDscNode</span></span>](./Register-AzureRmAutomationDscNode.md)

[<span data-ttu-id="0928e-159">Set-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="0928e-159">Set-AzureRmAutomationDscNode</span></span>](./Set-AzureRmAutomationDscNode.md)

[<span data-ttu-id="0928e-160">Cancelar registro-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="0928e-160">Unregister-AzureRmAutomationDscNode</span></span>](./Unregister-AzureRmAutomationDscNode.md)


