---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 6493186F-064B-45B7-8DFD-7799B1F2E5C9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNode.md
ms.openlocfilehash: 51d7df7f6b1e99188e5be31537700f4eef019053
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431204"
---
# <span data-ttu-id="78fa6-101">Get-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="78fa6-101">Get-AzureRmAutomationDscNode</span></span>

## <span data-ttu-id="78fa6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="78fa6-102">SYNOPSIS</span></span>
<span data-ttu-id="78fa6-103">Obtém nós DSC da automação.</span><span class="sxs-lookup"><span data-stu-id="78fa6-103">Gets DSC nodes from Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="78fa6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="78fa6-104">SYNTAX</span></span>

### <span data-ttu-id="78fa6-105">ByAll (padrão)</span><span class="sxs-lookup"><span data-stu-id="78fa6-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationDscNode [-Status <DscNodeStatus>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="78fa6-106">ById</span><span class="sxs-lookup"><span data-stu-id="78fa6-106">ById</span></span>
```
Get-AzureRmAutomationDscNode -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="78fa6-107">ByName</span><span class="sxs-lookup"><span data-stu-id="78fa6-107">ByName</span></span>
```
Get-AzureRmAutomationDscNode [-Status <DscNodeStatus>] -Name <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="78fa6-108">ByNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="78fa6-108">ByNodeConfiguration</span></span>
```
Get-AzureRmAutomationDscNode [-Status <DscNodeStatus>] -NodeConfigurationName <String>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="78fa6-109">ByConfiguration</span><span class="sxs-lookup"><span data-stu-id="78fa6-109">ByConfiguration</span></span>
```
Get-AzureRmAutomationDscNode -ConfigurationName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="78fa6-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="78fa6-110">DESCRIPTION</span></span>
<span data-ttu-id="78fa6-111">O cmdlet **Get-AzureRmAutomationDscNode** Obtém os nós DSC (configuração de estado desejado APS) da automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="78fa6-111">The **Get-AzureRmAutomationDscNode** cmdlet gets APS Desired State Configuration (DSC) nodes from Azure Automation.</span></span>

## <span data-ttu-id="78fa6-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="78fa6-112">EXAMPLES</span></span>

### <span data-ttu-id="78fa6-113">Exemplo 1: obter todos os nós DSC</span><span class="sxs-lookup"><span data-stu-id="78fa6-113">Example 1: Get all DSC nodes</span></span>
```
PS C:\>Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="78fa6-114">Esse comando obtém metadados para todos os nós DSC na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="78fa6-114">This command gets metadata for all DSC nodes in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="78fa6-115">Exemplo 2: obter todos os nós DSC para uma configuração DSC</span><span class="sxs-lookup"><span data-stu-id="78fa6-115">Example 2: Get all DSC nodes for a DSC configuration</span></span>
```
PS C:\>Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ConfigurationName "ContosoConfiguration"
```

<span data-ttu-id="78fa6-116">Esse comando obtém metadados para todos os nós DSC da conta de automação chamados Contoso17 que são mapeados para uma configuração de nó DSC que foi gerada pelo ContosoConfiguration de configuração DSC.</span><span class="sxs-lookup"><span data-stu-id="78fa6-116">This command gets metadata for all DSC nodes in the Automation account named Contoso17 that are mapped to a DSC node configuration which was generated by DSC configuration ContosoConfiguration.</span></span>

### <span data-ttu-id="78fa6-117">Exemplo 3: obter um nó DSC por ID</span><span class="sxs-lookup"><span data-stu-id="78fa6-117">Example 3: Get a DSC node by ID</span></span>
```
PS C:\>Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

<span data-ttu-id="78fa6-118">Esse comando obtém metadados em um nó DSC com a ID especificada na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="78fa6-118">This command gets metadata on a DSC node with the specified ID in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="78fa6-119">Exemplo 4: obter um nó DSC por nome</span><span class="sxs-lookup"><span data-stu-id="78fa6-119">Example 4: Get a DSC node by name</span></span>
```
PS C:\>Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
```

<span data-ttu-id="78fa6-120">Esse comando obtém metadados em um nó DSC com o nome Computer14 na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="78fa6-120">This command gets metadata on a DSC node with the name Computer14 in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="78fa6-121">Exemplo 5: obter todos os nós DSC mapeados para uma configuração de nó DSC</span><span class="sxs-lookup"><span data-stu-id="78fa6-121">Example 5: Get all DSC nodes mapped to a DSC node configuration</span></span>
```
PS C:\>Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeConfigurationName "ContosoConfiguration.webserver"
```

<span data-ttu-id="78fa6-122">Esse comando obtém metadados sobre todos os nós DSC da conta de automação chamados Contoso17 que são mapeados para uma configuração de nó DSC nomeada ContosoConfiguration. WebServer.</span><span class="sxs-lookup"><span data-stu-id="78fa6-122">This command gets metadata on all DSC nodes in the Automation account named Contoso17 that are mapped to a DSC node configuration named ContosoConfiguration.webserver.</span></span>

## <span data-ttu-id="78fa6-123">OS</span><span class="sxs-lookup"><span data-stu-id="78fa6-123">PARAMETERS</span></span>

### <span data-ttu-id="78fa6-124">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="78fa6-124">-AutomationAccountName</span></span>
<span data-ttu-id="78fa6-125">Especifica o nome da conta de automação que contém os nós DSC que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="78fa6-125">Specifies the name of the Automation account that contains the DSC nodes that this cmdlet gets.</span></span>

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

### <span data-ttu-id="78fa6-126">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="78fa6-126">-ConfigurationName</span></span>
<span data-ttu-id="78fa6-127">Especifica o nome de uma configuração DSC.</span><span class="sxs-lookup"><span data-stu-id="78fa6-127">Specifies the name of a DSC configuration.</span></span>
<span data-ttu-id="78fa6-128">Esse cmdlet obtém nós DSC que correspondem às configurações de nó geradas pela configuração que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="78fa6-128">This cmdlet gets DSC nodes that match the node configurations generated from the configuration that this parameter specifies.</span></span>

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

### <span data-ttu-id="78fa6-129">-ID</span><span class="sxs-lookup"><span data-stu-id="78fa6-129">-Id</span></span>
<span data-ttu-id="78fa6-130">Especifica a ID exclusiva do nó DSC que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="78fa6-130">Specifies the unique ID of the DSC node that this cmdlet gets.</span></span>

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

### <span data-ttu-id="78fa6-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="78fa6-131">-Name</span></span>
<span data-ttu-id="78fa6-132">Especifica o nome de um nó DSC que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="78fa6-132">Specifies the name of a DSC node that this cmdlet gets.</span></span>

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

### <span data-ttu-id="78fa6-133">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="78fa6-133">-NodeConfigurationName</span></span>
<span data-ttu-id="78fa6-134">Especifica o nome de uma configuração de nó obtida por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78fa6-134">Specifies the name of a node configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="78fa6-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78fa6-135">-ResourceGroupName</span></span>
<span data-ttu-id="78fa6-136">Especifica o nome de um grupo de recursos em que esse cmdlet obtém nós DSC.</span><span class="sxs-lookup"><span data-stu-id="78fa6-136">Specifies the name of a resource group in which this cmdlet gets DSC nodes.</span></span>

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

### <span data-ttu-id="78fa6-137">-Status</span><span class="sxs-lookup"><span data-stu-id="78fa6-137">-Status</span></span>
<span data-ttu-id="78fa6-138">Especifica o status dos nós DSC que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="78fa6-138">Specifies the status of the DSC nodes that this cmdlet gets.</span></span>
<span data-ttu-id="78fa6-139">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="78fa6-139">Valid values are:</span></span> 

- <span data-ttu-id="78fa6-140">CLS</span><span class="sxs-lookup"><span data-stu-id="78fa6-140">Compliant</span></span> 
- <span data-ttu-id="78fa6-141">Não compatível</span><span class="sxs-lookup"><span data-stu-id="78fa6-141">NotCompliant</span></span>
- <span data-ttu-id="78fa6-142">Conseguiu</span><span class="sxs-lookup"><span data-stu-id="78fa6-142">Failed</span></span>
- <span data-ttu-id="78fa6-143">Pending</span><span class="sxs-lookup"><span data-stu-id="78fa6-143">Pending</span></span> 
- <span data-ttu-id="78fa6-144">Recebi</span><span class="sxs-lookup"><span data-stu-id="78fa6-144">Received</span></span>
- <span data-ttu-id="78fa6-145">Respondendo</span><span class="sxs-lookup"><span data-stu-id="78fa6-145">Unresponsive</span></span>

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

### <span data-ttu-id="78fa6-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78fa6-146">-DefaultProfile</span></span>
<span data-ttu-id="78fa6-147">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="78fa6-147">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="78fa6-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78fa6-148">CommonParameters</span></span>
<span data-ttu-id="78fa6-149">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78fa6-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78fa6-150">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78fa6-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78fa6-151">SENSORES</span><span class="sxs-lookup"><span data-stu-id="78fa6-151">INPUTS</span></span>

## <span data-ttu-id="78fa6-152">EXIBE</span><span class="sxs-lookup"><span data-stu-id="78fa6-152">OUTPUTS</span></span>

### <span data-ttu-id="78fa6-153">Microsoft. Azure. Commands. Automation. Model. DscNode</span><span class="sxs-lookup"><span data-stu-id="78fa6-153">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="78fa6-154">INFORMA</span><span class="sxs-lookup"><span data-stu-id="78fa6-154">NOTES</span></span>

## <span data-ttu-id="78fa6-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="78fa6-155">RELATED LINKS</span></span>

[<span data-ttu-id="78fa6-156">Register-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="78fa6-156">Register-AzureRmAutomationDscNode</span></span>](./Register-AzureRmAutomationDscNode.md)

[<span data-ttu-id="78fa6-157">Set-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="78fa6-157">Set-AzureRmAutomationDscNode</span></span>](./Set-AzureRmAutomationDscNode.md)

[<span data-ttu-id="78fa6-158">Cancelar registro-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="78fa6-158">Unregister-AzureRmAutomationDscNode</span></span>](./Unregister-AzureRmAutomationDscNode.md)


