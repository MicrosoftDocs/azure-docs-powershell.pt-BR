---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/New-azstorageobjectreplicationpolicyrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageObjectReplicationPolicyRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageObjectReplicationPolicyRule.md
ms.openlocfilehash: c8d41300250e41548cf949248b02c819b7da497f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94112071"
---
# <span data-ttu-id="58d1b-101">New-AzStorageObjectReplicationPolicyRule</span><span class="sxs-lookup"><span data-stu-id="58d1b-101">New-AzStorageObjectReplicationPolicyRule</span></span>

## <span data-ttu-id="58d1b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="58d1b-102">SYNOPSIS</span></span>
<span data-ttu-id="58d1b-103">Cria uma regra de política de replicação de objetos.</span><span class="sxs-lookup"><span data-stu-id="58d1b-103">Creates an object replication policy rule.</span></span>

## <span data-ttu-id="58d1b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="58d1b-104">SYNTAX</span></span>

```
New-AzStorageObjectReplicationPolicyRule -SourceContainer <String> -DestinationContainer <String>
 [-PrefixMatch <String[]>] [-MinCreationTime <DateTime>] [-RuleId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="58d1b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="58d1b-105">DESCRIPTION</span></span>
<span data-ttu-id="58d1b-106">O cmdlet **Get-AzStorageObjectReplicationPolicy** cria uma regra de política de replicação de objetos, que será usada no cmdlet Set-AzStorageObjectReplicationPolicy.</span><span class="sxs-lookup"><span data-stu-id="58d1b-106">The **Get-AzStorageObjectReplicationPolicy** cmdlet creates an object replication policy rule, which will be used in Set-AzStorageObjectReplicationPolicy cmdlet.</span></span>

## <span data-ttu-id="58d1b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="58d1b-107">EXAMPLES</span></span>

### <span data-ttu-id="58d1b-108">Exemplo 1: criar uma regra de política de replicação de objeto com apenas uma conta de origem e de destino e mostrar suas propriedades</span><span class="sxs-lookup"><span data-stu-id="58d1b-108">Example 1: Create an object replication policy rule with only source and destination account, and show its properties</span></span>
```
PS C:\> $rule1 = New-AzStorageObjectReplicationPolicyRule -SourceContainer src1 -DestinationContainer dest1 

PS C:\> $rule1

RuleId SourceContainer DestinationContainer Filters.PrefixMatch Filters.MinCreationTime
------ --------------- -------------------- ------------------- -----------------------
       src1            dest1                {}
```

<span data-ttu-id="58d1b-109">Esse comando cria uma regra de política de replicação de objeto com apenas uma conta de origem e de destino e mostra suas propriedades.</span><span class="sxs-lookup"><span data-stu-id="58d1b-109">This command creates an object replication policy rule with only source and destination account, and show its properties.</span></span>

### <span data-ttu-id="58d1b-110">Exemplo 2: criar uma regra de política de replicação de objeto com todas as propriedades e mostrar suas propriedades</span><span class="sxs-lookup"><span data-stu-id="58d1b-110">Example 2: Create an object replication policy rule with all properties, and show its properties</span></span>
```
PS C:\> $rule2 = New-AzStorageObjectReplicationPolicyRule -SourceContainer src -DestinationContainer dest -MinCreationTime 2019-01-01T16:00:00Z -PrefixMatch a,abc,dd

PS C:\> $rule2

RuleId SourceContainer DestinationContainer Filters.PrefixMatch Filters.MinCreationTime
------ --------------- -------------------- ------------------- -----------------------
       src             dest                 {a, abc, dd}        2019-01-01T16:00:00Z
```

<span data-ttu-id="58d1b-111">Esse comando uma regra de política de replicação de objeto com todas as propriedades e mostrar suas propriedades.</span><span class="sxs-lookup"><span data-stu-id="58d1b-111">This command an object replication policy rule with all properties, and show its properties.</span></span>

## <span data-ttu-id="58d1b-112">OS</span><span class="sxs-lookup"><span data-stu-id="58d1b-112">PARAMETERS</span></span>

### <span data-ttu-id="58d1b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58d1b-113">-DefaultProfile</span></span>
<span data-ttu-id="58d1b-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="58d1b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58d1b-115">-DestinationContainer</span><span class="sxs-lookup"><span data-stu-id="58d1b-115">-DestinationContainer</span></span>
<span data-ttu-id="58d1b-116">O nome do contêiner de destino para replicação.</span><span class="sxs-lookup"><span data-stu-id="58d1b-116">The Destination Container name to replicate to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58d1b-117">-MinCreationTime</span><span class="sxs-lookup"><span data-stu-id="58d1b-117">-MinCreationTime</span></span>
<span data-ttu-id="58d1b-118">Os BLOBs criados após o horário serão duplicados para o destino..</span><span class="sxs-lookup"><span data-stu-id="58d1b-118">Blobs created after the time will be replicated to the destination..</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58d1b-119">-PrefixMatch</span><span class="sxs-lookup"><span data-stu-id="58d1b-119">-PrefixMatch</span></span>
<span data-ttu-id="58d1b-120">Filtra os resultados para replicar somente BLOBs cujos nomes começam com o prefixo especificado.</span><span class="sxs-lookup"><span data-stu-id="58d1b-120">Filters the results to replicate only blobs whose names begin with the specified prefix.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58d1b-121">-RuleId</span><span class="sxs-lookup"><span data-stu-id="58d1b-121">-RuleId</span></span>
<span data-ttu-id="58d1b-122">ID da regra de replicação do objeto.</span><span class="sxs-lookup"><span data-stu-id="58d1b-122">Object Replication Rule Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58d1b-123">-SourceContainer</span><span class="sxs-lookup"><span data-stu-id="58d1b-123">-SourceContainer</span></span>
<span data-ttu-id="58d1b-124">O nome do contêiner de origem para replicação.</span><span class="sxs-lookup"><span data-stu-id="58d1b-124">The Source Container name to replicate from.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58d1b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58d1b-125">CommonParameters</span></span>
<span data-ttu-id="58d1b-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58d1b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58d1b-127">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58d1b-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58d1b-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="58d1b-128">INPUTS</span></span>

### <span data-ttu-id="58d1b-129">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="58d1b-129">None</span></span>

## <span data-ttu-id="58d1b-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="58d1b-130">OUTPUTS</span></span>

### <span data-ttu-id="58d1b-131">Microsoft. Azure. Commands. Management. Storage. Models. PSObjectReplicationPolicyRule</span><span class="sxs-lookup"><span data-stu-id="58d1b-131">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicyRule</span></span>

## <span data-ttu-id="58d1b-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="58d1b-132">NOTES</span></span>

## <span data-ttu-id="58d1b-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="58d1b-133">RELATED LINKS</span></span>
