---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountbatchconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountBatchConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountBatchConfiguration.md
ms.openlocfilehash: 26a2e414f05fc0aeb209afa946ae168c59ea4ff8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117582"
---
# <span data-ttu-id="c6dc9-101">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="c6dc9-101">Get-AzIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="c6dc9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c6dc9-102">SYNOPSIS</span></span>
<span data-ttu-id="c6dc9-103">Obtém uma configuração de lote de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="c6dc9-103">Gets an integration account batch configuration.</span></span>

## <span data-ttu-id="c6dc9-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c6dc9-104">SYNTAX</span></span>

### <span data-ttu-id="c6dc9-105">ByIntegrationAccount (Padrão)</span><span class="sxs-lookup"><span data-stu-id="c6dc9-105">ByIntegrationAccount (Default)</span></span>
```
Get-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c6dc9-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="c6dc9-106">ByInputObject</span></span>
```
Get-AzIntegrationAccountBatchConfiguration -ParentObject <IntegrationAccount> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c6dc9-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c6dc9-107">ByResourceId</span></span>
```
Get-AzIntegrationAccountBatchConfiguration -ParentResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c6dc9-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="c6dc9-108">DESCRIPTION</span></span>
<span data-ttu-id="c6dc9-109">O cmdlet **Get-AzIntegrationAccountBatchConfiguration** obtém uma configuração em lotes de uma conta de integração.</span><span class="sxs-lookup"><span data-stu-id="c6dc9-109">The **Get-AzIntegrationAccountBatchConfiguration** cmdlet gets an batch configuration from an integration account.</span></span>

## <span data-ttu-id="c6dc9-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c6dc9-110">EXAMPLES</span></span>

### <span data-ttu-id="c6dc9-111">Exemplo 1: Obter uma configuração em lotes por parâmetros</span><span class="sxs-lookup"><span data-stu-id="c6dc9-111">Example 1: Get a batch configuration by parameters</span></span>
```powershell
PS C:\> Get-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig"

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="c6dc9-112">Obter uma configuração em lotes chamada "sampleBatchConfig" localizada na conta de integração "sampleIntegrationAccount", que está contida no grupo de recursos "sampleResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="c6dc9-112">Get a batch configuration named "sampleBatchConfig" located in the integration account "sampleIntegrationAccount" which is contained in the resource group "sampleResourceGroup".</span></span>

### <span data-ttu-id="c6dc9-113">Exemplo 2: Listar todas as configurações em lotes em uma conta de integração por parâmetros</span><span class="sxs-lookup"><span data-stu-id="c6dc9-113">Example 2: List all batch configurations in an integration account by parameters</span></span>
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

<span data-ttu-id="c6dc9-114">Obter todas as configurações de lote localizadas na conta de integração "sampleIntegrationAccount", que está contida no grupo de recursos "sampleResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="c6dc9-114">Get all batch configurations located in the integration account "sampleIntegrationAccount" which is contained in the resource group "sampleResourceGroup".</span></span>

## <span data-ttu-id="c6dc9-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c6dc9-115">PARAMETERS</span></span>

### <span data-ttu-id="c6dc9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6dc9-116">-DefaultProfile</span></span>
<span data-ttu-id="c6dc9-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c6dc9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6dc9-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="c6dc9-118">-Name</span></span>
<span data-ttu-id="c6dc9-119">O nome de configuração de lote da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="c6dc9-119">The integration account batch configuration name.</span></span>

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

### <span data-ttu-id="c6dc9-120">-ParentName</span><span class="sxs-lookup"><span data-stu-id="c6dc9-120">-ParentName</span></span>
<span data-ttu-id="c6dc9-121">O nome da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="c6dc9-121">The integration account name.</span></span>

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

### <span data-ttu-id="c6dc9-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="c6dc9-122">-ParentObject</span></span>
<span data-ttu-id="c6dc9-123">Um objeto de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="c6dc9-123">An integration account object.</span></span>

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

### <span data-ttu-id="c6dc9-124">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="c6dc9-124">-ParentResourceId</span></span>
<span data-ttu-id="c6dc9-125">A ID de recurso da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="c6dc9-125">The integration account resource id.</span></span>

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

### <span data-ttu-id="c6dc9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6dc9-126">-ResourceGroupName</span></span>
<span data-ttu-id="c6dc9-127">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c6dc9-127">The resource group name.</span></span>

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

### <span data-ttu-id="c6dc9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6dc9-128">CommonParameters</span></span>
<span data-ttu-id="c6dc9-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6dc9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6dc9-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6dc9-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6dc9-131">Entradas</span><span class="sxs-lookup"><span data-stu-id="c6dc9-131">INPUTS</span></span>

### <span data-ttu-id="c6dc9-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="c6dc9-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

### <span data-ttu-id="c6dc9-133">System.String</span><span class="sxs-lookup"><span data-stu-id="c6dc9-133">System.String</span></span>

## <span data-ttu-id="c6dc9-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="c6dc9-134">OUTPUTS</span></span>

### <span data-ttu-id="c6dc9-135">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="c6dc9-135">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="c6dc9-136">Notas</span><span class="sxs-lookup"><span data-stu-id="c6dc9-136">NOTES</span></span>

## <span data-ttu-id="c6dc9-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c6dc9-137">RELATED LINKS</span></span>
