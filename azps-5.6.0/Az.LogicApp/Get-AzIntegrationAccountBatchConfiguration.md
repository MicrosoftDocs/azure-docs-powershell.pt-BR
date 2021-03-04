---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/powershell/module/az.logicapp/get-azintegrationaccountbatchconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountBatchConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountBatchConfiguration.md
ms.openlocfilehash: 722f2bd79230de11c12ab0448fb39ed3ad49f00d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886474"
---
# <span data-ttu-id="220be-101">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="220be-101">Get-AzIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="220be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="220be-102">SYNOPSIS</span></span>
<span data-ttu-id="220be-103">Obtém uma configuração de lote de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="220be-103">Gets an integration account batch configuration.</span></span>

## <span data-ttu-id="220be-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="220be-104">SYNTAX</span></span>

### <span data-ttu-id="220be-105">ByIntegrationAccount (Padrão)</span><span class="sxs-lookup"><span data-stu-id="220be-105">ByIntegrationAccount (Default)</span></span>
```
Get-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="220be-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="220be-106">ByInputObject</span></span>
```
Get-AzIntegrationAccountBatchConfiguration -ParentObject <IntegrationAccount> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="220be-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="220be-107">ByResourceId</span></span>
```
Get-AzIntegrationAccountBatchConfiguration -ParentResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="220be-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="220be-108">DESCRIPTION</span></span>
<span data-ttu-id="220be-109">O cmdlet **Get-AzIntegrationAccountBatchConfiguration** obtém uma configuração em lotes de uma conta de integração.</span><span class="sxs-lookup"><span data-stu-id="220be-109">The **Get-AzIntegrationAccountBatchConfiguration** cmdlet gets an batch configuration from an integration account.</span></span>

## <span data-ttu-id="220be-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="220be-110">EXAMPLES</span></span>

### <span data-ttu-id="220be-111">Exemplo 1: Obter uma configuração em lote por parâmetros</span><span class="sxs-lookup"><span data-stu-id="220be-111">Example 1: Get a batch configuration by parameters</span></span>
```powershell
PS C:\> Get-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig"

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="220be-112">Obter uma configuração em lote denominada "sampleBatchConfig" localizada na conta de integração "sampleIntegrationAccount" que está contida no grupo de recursos "sampleResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="220be-112">Get a batch configuration named "sampleBatchConfig" located in the integration account "sampleIntegrationAccount" which is contained in the resource group "sampleResourceGroup".</span></span>

### <span data-ttu-id="220be-113">Exemplo 2: Listar todas as configurações em lotes em uma conta de integração por parâmetros</span><span class="sxs-lookup"><span data-stu-id="220be-113">Example 2: List all batch configurations in an integration account by parameters</span></span>
```powershell
PS C:\> Get-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount"

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig2
Name       : sampleBatchConfig2
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="220be-114">Obter todas as configurações em lote localizadas na conta de integração "sampleIntegrationAccount" que está contida no grupo de recursos "sampleResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="220be-114">Get all batch configurations located in the integration account "sampleIntegrationAccount" which is contained in the resource group "sampleResourceGroup".</span></span>

## <span data-ttu-id="220be-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="220be-115">PARAMETERS</span></span>

### <span data-ttu-id="220be-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="220be-116">-DefaultProfile</span></span>
<span data-ttu-id="220be-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="220be-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="220be-118">-Name</span><span class="sxs-lookup"><span data-stu-id="220be-118">-Name</span></span>
<span data-ttu-id="220be-119">O nome de configuração de lote da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="220be-119">The integration account batch configuration name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BatchConfigurationName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="220be-120">-ParentName</span><span class="sxs-lookup"><span data-stu-id="220be-120">-ParentName</span></span>
<span data-ttu-id="220be-121">O nome da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="220be-121">The integration account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccount
Aliases: IntegrationAccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="220be-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="220be-122">-ParentObject</span></span>
<span data-ttu-id="220be-123">Um objeto de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="220be-123">An integration account object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Logic.Models.IntegrationAccount
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="220be-124">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="220be-124">-ParentResourceId</span></span>
<span data-ttu-id="220be-125">A ID do recurso de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="220be-125">The integration account resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="220be-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="220be-126">-ResourceGroupName</span></span>
<span data-ttu-id="220be-127">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="220be-127">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="220be-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="220be-128">CommonParameters</span></span>
<span data-ttu-id="220be-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="220be-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="220be-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="220be-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="220be-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="220be-131">INPUTS</span></span>

### <span data-ttu-id="220be-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="220be-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

### <span data-ttu-id="220be-133">System.String</span><span class="sxs-lookup"><span data-stu-id="220be-133">System.String</span></span>

## <span data-ttu-id="220be-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="220be-134">OUTPUTS</span></span>

### <span data-ttu-id="220be-135">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="220be-135">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="220be-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="220be-136">NOTES</span></span>

## <span data-ttu-id="220be-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="220be-137">RELATED LINKS</span></span>
