---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountbatchconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountBatchConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountBatchConfiguration.md
ms.openlocfilehash: 26a2e414f05fc0aeb209afa946ae168c59ea4ff8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260137"
---
# <span data-ttu-id="0b480-101">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="0b480-101">Get-AzIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="0b480-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0b480-102">SYNOPSIS</span></span>
<span data-ttu-id="0b480-103">Obtém uma configuração em lotes da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="0b480-103">Gets an integration account batch configuration.</span></span>

## <span data-ttu-id="0b480-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0b480-104">SYNTAX</span></span>

### <span data-ttu-id="0b480-105">ByIntegrationAccount (padrão)</span><span class="sxs-lookup"><span data-stu-id="0b480-105">ByIntegrationAccount (Default)</span></span>
```
Get-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0b480-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="0b480-106">ByInputObject</span></span>
```
Get-AzIntegrationAccountBatchConfiguration -ParentObject <IntegrationAccount> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0b480-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="0b480-107">ByResourceId</span></span>
```
Get-AzIntegrationAccountBatchConfiguration -ParentResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0b480-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0b480-108">DESCRIPTION</span></span>
<span data-ttu-id="0b480-109">O cmdlet **Get-AzIntegrationAccountBatchConfiguration** Obtém uma configuração em lotes de uma conta de integração.</span><span class="sxs-lookup"><span data-stu-id="0b480-109">The **Get-AzIntegrationAccountBatchConfiguration** cmdlet gets an batch configuration from an integration account.</span></span>

## <span data-ttu-id="0b480-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0b480-110">EXAMPLES</span></span>

### <span data-ttu-id="0b480-111">Exemplo 1: obter uma configuração em lotes por parâmetros</span><span class="sxs-lookup"><span data-stu-id="0b480-111">Example 1: Get a batch configuration by parameters</span></span>
```powershell
PS C:\> Get-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig"

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="0b480-112">Obtenha uma configuração em lotes chamada "sampleBatchConfig" localizada na conta de integração "sampleIntegrationAccount" que está contida no grupo de recursos "sampleResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="0b480-112">Get a batch configuration named "sampleBatchConfig" located in the integration account "sampleIntegrationAccount" which is contained in the resource group "sampleResourceGroup".</span></span>

### <span data-ttu-id="0b480-113">Exemplo 2: listar todas as configurações em lotes em uma conta de integração por parâmetros</span><span class="sxs-lookup"><span data-stu-id="0b480-113">Example 2: List all batch configurations in an integration account by parameters</span></span>
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

<span data-ttu-id="0b480-114">Obtenha todas as configurações em lotes localizadas na conta de integração "sampleIntegrationAccount" que está contida no grupo de recursos "sampleResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="0b480-114">Get all batch configurations located in the integration account "sampleIntegrationAccount" which is contained in the resource group "sampleResourceGroup".</span></span>

## <span data-ttu-id="0b480-115">OS</span><span class="sxs-lookup"><span data-stu-id="0b480-115">PARAMETERS</span></span>

### <span data-ttu-id="0b480-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b480-116">-DefaultProfile</span></span>
<span data-ttu-id="0b480-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0b480-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b480-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="0b480-118">-Name</span></span>
<span data-ttu-id="0b480-119">O nome de configuração em lotes da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="0b480-119">The integration account batch configuration name.</span></span>

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

### <span data-ttu-id="0b480-120">-ParentName</span><span class="sxs-lookup"><span data-stu-id="0b480-120">-ParentName</span></span>
<span data-ttu-id="0b480-121">O nome da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="0b480-121">The integration account name.</span></span>

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

### <span data-ttu-id="0b480-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="0b480-122">-ParentObject</span></span>
<span data-ttu-id="0b480-123">Um objeto de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="0b480-123">An integration account object.</span></span>

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

### <span data-ttu-id="0b480-124">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="0b480-124">-ParentResourceId</span></span>
<span data-ttu-id="0b480-125">A ID do recurso da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="0b480-125">The integration account resource id.</span></span>

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

### <span data-ttu-id="0b480-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b480-126">-ResourceGroupName</span></span>
<span data-ttu-id="0b480-127">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0b480-127">The resource group name.</span></span>

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

### <span data-ttu-id="0b480-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b480-128">CommonParameters</span></span>
<span data-ttu-id="0b480-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b480-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b480-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b480-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b480-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0b480-131">INPUTS</span></span>

### <span data-ttu-id="0b480-132">Microsoft. Azure. Management. Logic. Models. IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="0b480-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

### <span data-ttu-id="0b480-133">System. String</span><span class="sxs-lookup"><span data-stu-id="0b480-133">System.String</span></span>

## <span data-ttu-id="0b480-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0b480-134">OUTPUTS</span></span>

### <span data-ttu-id="0b480-135">Microsoft. Azure. Commands. LogicApp. Models. PSIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="0b480-135">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="0b480-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0b480-136">NOTES</span></span>

## <span data-ttu-id="0b480-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0b480-137">RELATED LINKS</span></span>
