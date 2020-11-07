---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2triggersubscriptionstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2TriggerSubscriptionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2TriggerSubscriptionStatus.md
ms.openlocfilehash: 62418f0840e2bbeef016d53c3136f155c4de055f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93778355"
---
# <span data-ttu-id="df74f-101">Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="df74f-101">Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>

## <span data-ttu-id="df74f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="df74f-102">SYNOPSIS</span></span>
<span data-ttu-id="df74f-103">Obtenha o status da assinatura do gatilho de evento para os eventos de serviço externo especificados.</span><span class="sxs-lookup"><span data-stu-id="df74f-103">Get the status of the subscription for the event trigger to the specified external service events.</span></span>

## <span data-ttu-id="df74f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="df74f-104">SYNTAX</span></span>

### <span data-ttu-id="df74f-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="df74f-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2TriggerSubscriptionStatus [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="df74f-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="df74f-106">ByInputObject</span></span>
```
Get-AzDataFactoryV2TriggerSubscriptionStatus [-InputObject] <PSTrigger>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="df74f-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="df74f-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2TriggerSubscriptionStatus [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="df74f-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="df74f-108">DESCRIPTION</span></span>
<span data-ttu-id="df74f-109">Esse comando obtém o status da assinatura do gatilho de evento para os eventos de serviço externo especificados.</span><span class="sxs-lookup"><span data-stu-id="df74f-109">This command gets the status of the subscription for the event trigger to the specified external service events.</span></span> <span data-ttu-id="df74f-110">O gatilho não pode ser iniciado até que o status retornado seja "habilitado".</span><span class="sxs-lookup"><span data-stu-id="df74f-110">The trigger can't be started until the returned status is "Enabled".</span></span>

## <span data-ttu-id="df74f-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="df74f-111">EXAMPLES</span></span>

### <span data-ttu-id="df74f-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="df74f-112">Example 1</span></span>
```
PS C:\> Get-AzDataFactoryV2TriggerSubscriptionStatus -ResourceGroupName ADF -DataFactoryName WikiADF -Name Trigger1

TriggerName Status
----------- ------
Trigger1    Enabled
```

<span data-ttu-id="df74f-113">Esse comando receberá o status do gatilho Subscribtion para BlobEnetTrigger1 para os eventos do serviço externo.</span><span class="sxs-lookup"><span data-stu-id="df74f-113">This command will get the status of the subscribtion for BlobEnetTrigger1 trigger to the external service events.</span></span>

## <span data-ttu-id="df74f-114">OS</span><span class="sxs-lookup"><span data-stu-id="df74f-114">PARAMETERS</span></span>

### <span data-ttu-id="df74f-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="df74f-115">-DataFactoryName</span></span>
<span data-ttu-id="df74f-116">O nome do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="df74f-116">The data factory name.</span></span>

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

### <span data-ttu-id="df74f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df74f-117">-DefaultProfile</span></span>
<span data-ttu-id="df74f-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="df74f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df74f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="df74f-119">-InputObject</span></span>
<span data-ttu-id="df74f-120">O objeto Trigger.</span><span class="sxs-lookup"><span data-stu-id="df74f-120">The trigger object.</span></span>

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

### <span data-ttu-id="df74f-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="df74f-121">-Name</span></span>
<span data-ttu-id="df74f-122">O nome do disparador.</span><span class="sxs-lookup"><span data-stu-id="df74f-122">The trigger name.</span></span>

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

### <span data-ttu-id="df74f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df74f-123">-ResourceGroupName</span></span>
<span data-ttu-id="df74f-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="df74f-124">The resource group name.</span></span>

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

### <span data-ttu-id="df74f-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="df74f-125">-ResourceId</span></span>
<span data-ttu-id="df74f-126">A ID do recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="df74f-126">The Azure resource ID.</span></span>

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

### <span data-ttu-id="df74f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df74f-127">CommonParameters</span></span>
<span data-ttu-id="df74f-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df74f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df74f-129">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df74f-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df74f-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="df74f-130">INPUTS</span></span>

### <span data-ttu-id="df74f-131">System. String</span><span class="sxs-lookup"><span data-stu-id="df74f-131">System.String</span></span>
<span data-ttu-id="df74f-132">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="df74f-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="df74f-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="df74f-133">OUTPUTS</span></span>

### <span data-ttu-id="df74f-134">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="df74f-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span></span>

## <span data-ttu-id="df74f-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="df74f-135">NOTES</span></span>

## <span data-ttu-id="df74f-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="df74f-136">RELATED LINKS</span></span>

