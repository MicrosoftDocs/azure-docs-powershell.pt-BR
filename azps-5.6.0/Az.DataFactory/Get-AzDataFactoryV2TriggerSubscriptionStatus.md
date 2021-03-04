---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactoryv2triggersubscriptionstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2TriggerSubscriptionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2TriggerSubscriptionStatus.md
ms.openlocfilehash: a83028b47d487f4bbb2732497d7e9eefd01882ce
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888275"
---
# <span data-ttu-id="b8ddc-101">Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="b8ddc-101">Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>

## <span data-ttu-id="b8ddc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8ddc-102">SYNOPSIS</span></span>
<span data-ttu-id="b8ddc-103">Obter o status da assinatura do gatilho de evento para os eventos de serviço externo especificados.</span><span class="sxs-lookup"><span data-stu-id="b8ddc-103">Get the status of the subscription for the event trigger to the specified external service events.</span></span>

## <span data-ttu-id="b8ddc-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b8ddc-104">SYNTAX</span></span>

### <span data-ttu-id="b8ddc-105">ByFactoryName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="b8ddc-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2TriggerSubscriptionStatus [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b8ddc-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="b8ddc-106">ByInputObject</span></span>
```
Get-AzDataFactoryV2TriggerSubscriptionStatus [-InputObject] <PSTrigger>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b8ddc-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b8ddc-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2TriggerSubscriptionStatus [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b8ddc-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b8ddc-108">DESCRIPTION</span></span>
<span data-ttu-id="b8ddc-109">Este comando obtém o status da assinatura do gatilho de evento para os eventos de serviço externo especificados.</span><span class="sxs-lookup"><span data-stu-id="b8ddc-109">This command gets the status of the subscription for the event trigger to the specified external service events.</span></span> <span data-ttu-id="b8ddc-110">O gatilho não pode ser iniciado até que o status retornado seja "Habilitado".</span><span class="sxs-lookup"><span data-stu-id="b8ddc-110">The trigger can't be started until the returned status is "Enabled".</span></span>

## <span data-ttu-id="b8ddc-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b8ddc-111">EXAMPLES</span></span>

### <span data-ttu-id="b8ddc-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b8ddc-112">Example 1</span></span>
```
PS C:\> Get-AzDataFactoryV2TriggerSubscriptionStatus -ResourceGroupName ADF -DataFactoryName WikiADF -Name Trigger1

TriggerName Status
----------- ------
Trigger1    Enabled
```

<span data-ttu-id="b8ddc-113">Este comando obterá o status da subscrição para o gatilho BlobEnetTrigger1 para os eventos de serviço externos.</span><span class="sxs-lookup"><span data-stu-id="b8ddc-113">This command will get the status of the subscribtion for BlobEnetTrigger1 trigger to the external service events.</span></span>

## <span data-ttu-id="b8ddc-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b8ddc-114">PARAMETERS</span></span>

### <span data-ttu-id="b8ddc-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="b8ddc-115">-DataFactoryName</span></span>
<span data-ttu-id="b8ddc-116">O nome da fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="b8ddc-116">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8ddc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8ddc-117">-DefaultProfile</span></span>
<span data-ttu-id="b8ddc-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b8ddc-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8ddc-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b8ddc-119">-InputObject</span></span>
<span data-ttu-id="b8ddc-120">O objeto trigger.</span><span class="sxs-lookup"><span data-stu-id="b8ddc-120">The trigger object.</span></span>

```yaml
Type: PSTrigger
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b8ddc-121">-Name</span><span class="sxs-lookup"><span data-stu-id="b8ddc-121">-Name</span></span>
<span data-ttu-id="b8ddc-122">O nome do gatilho.</span><span class="sxs-lookup"><span data-stu-id="b8ddc-122">The trigger name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8ddc-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8ddc-123">-ResourceGroupName</span></span>
<span data-ttu-id="b8ddc-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b8ddc-124">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8ddc-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b8ddc-125">-ResourceId</span></span>
<span data-ttu-id="b8ddc-126">A ID de recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="b8ddc-126">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8ddc-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8ddc-127">CommonParameters</span></span>
<span data-ttu-id="b8ddc-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8ddc-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8ddc-129">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8ddc-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8ddc-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b8ddc-130">INPUTS</span></span>

### <span data-ttu-id="b8ddc-131">System.String</span><span class="sxs-lookup"><span data-stu-id="b8ddc-131">System.String</span></span>
<span data-ttu-id="b8ddc-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span><span class="sxs-lookup"><span data-stu-id="b8ddc-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="b8ddc-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b8ddc-133">OUTPUTS</span></span>

### <span data-ttu-id="b8ddc-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="b8ddc-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span></span>

## <span data-ttu-id="b8ddc-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="b8ddc-135">NOTES</span></span>

## <span data-ttu-id="b8ddc-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b8ddc-136">RELATED LINKS</span></span>

