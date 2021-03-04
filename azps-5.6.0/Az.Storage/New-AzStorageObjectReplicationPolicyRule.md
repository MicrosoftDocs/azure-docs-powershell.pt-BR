---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/New-azstorageobjectreplicationpolicyrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageObjectReplicationPolicyRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageObjectReplicationPolicyRule.md
ms.openlocfilehash: 8338f13829ebc3feff4c5a81fdfb3bd13934d90d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891957"
---
# <span data-ttu-id="5eaa2-101">New-AzStorageObjectReplicationPolicyRule</span><span class="sxs-lookup"><span data-stu-id="5eaa2-101">New-AzStorageObjectReplicationPolicyRule</span></span>

## <span data-ttu-id="5eaa2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5eaa2-102">SYNOPSIS</span></span>
<span data-ttu-id="5eaa2-103">Cria uma regra de política de replicação de objeto.</span><span class="sxs-lookup"><span data-stu-id="5eaa2-103">Creates an object replication policy rule.</span></span>

## <span data-ttu-id="5eaa2-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="5eaa2-104">SYNTAX</span></span>

```
New-AzStorageObjectReplicationPolicyRule -SourceContainer <String> -DestinationContainer <String>
 [-PrefixMatch <String[]>] [-MinCreationTime <DateTime>] [-RuleId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5eaa2-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="5eaa2-105">DESCRIPTION</span></span>
<span data-ttu-id="5eaa2-106">O cmdlet **Get-AzStorageObjectReplicationPolicy** cria uma regra de política de replicação de objeto, que será usada Set-AzStorageObjectReplicationPolicy cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5eaa2-106">The **Get-AzStorageObjectReplicationPolicy** cmdlet creates an object replication policy rule, which will be used in Set-AzStorageObjectReplicationPolicy cmdlet.</span></span>

## <span data-ttu-id="5eaa2-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5eaa2-107">EXAMPLES</span></span>

### <span data-ttu-id="5eaa2-108">Exemplo 1: criar uma regra de política de replicação de objeto com apenas conta de origem e destino e mostrar suas propriedades</span><span class="sxs-lookup"><span data-stu-id="5eaa2-108">Example 1: Create an object replication policy rule with only source and destination account, and show its properties</span></span>
```
PS C:\> $rule1 = New-AzStorageObjectReplicationPolicyRule -SourceContainer src1 -DestinationContainer dest1 

PS C:\> $rule1

RuleId SourceContainer DestinationContainer Filters.PrefixMatch Filters.MinCreationTime
------ --------------- -------------------- ------------------- -----------------------
       src1            dest1                {}
```

<span data-ttu-id="5eaa2-109">Este comando cria uma regra de política de replicação de objeto com apenas conta de origem e destino e mostra suas propriedades.</span><span class="sxs-lookup"><span data-stu-id="5eaa2-109">This command creates an object replication policy rule with only source and destination account, and show its properties.</span></span>

### <span data-ttu-id="5eaa2-110">Exemplo 2: criar uma regra de política de replicação de objeto com todas as propriedades e mostrar suas propriedades</span><span class="sxs-lookup"><span data-stu-id="5eaa2-110">Example 2: Create an object replication policy rule with all properties, and show its properties</span></span>
```
PS C:\> $rule2 = New-AzStorageObjectReplicationPolicyRule -SourceContainer src -DestinationContainer dest -MinCreationTime 2019-01-01T16:00:00Z -PrefixMatch a,abc,dd

PS C:\> $rule2

RuleId SourceContainer DestinationContainer Filters.PrefixMatch Filters.MinCreationTime
------ --------------- -------------------- ------------------- -----------------------
       src             dest                 {a, abc, dd}        2019-01-01T16:00:00Z
```

<span data-ttu-id="5eaa2-111">Este comando é uma regra de política de replicação de objeto com todas as propriedades e mostra suas propriedades.</span><span class="sxs-lookup"><span data-stu-id="5eaa2-111">This command an object replication policy rule with all properties, and show its properties.</span></span>

## <span data-ttu-id="5eaa2-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="5eaa2-112">PARAMETERS</span></span>

### <span data-ttu-id="5eaa2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5eaa2-113">-DefaultProfile</span></span>
<span data-ttu-id="5eaa2-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5eaa2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5eaa2-115">-DestinationContainer</span><span class="sxs-lookup"><span data-stu-id="5eaa2-115">-DestinationContainer</span></span>
<span data-ttu-id="5eaa2-116">O nome do Contêiner de Destino a ser replicado.</span><span class="sxs-lookup"><span data-stu-id="5eaa2-116">The Destination Container name to replicate to.</span></span>

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

### <span data-ttu-id="5eaa2-117">-MinCreationTime</span><span class="sxs-lookup"><span data-stu-id="5eaa2-117">-MinCreationTime</span></span>
<span data-ttu-id="5eaa2-118">Blobs criados após o horário serão replicados para o destino..</span><span class="sxs-lookup"><span data-stu-id="5eaa2-118">Blobs created after the time will be replicated to the destination..</span></span>

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

### <span data-ttu-id="5eaa2-119">-PrefixMatch</span><span class="sxs-lookup"><span data-stu-id="5eaa2-119">-PrefixMatch</span></span>
<span data-ttu-id="5eaa2-120">Filtra os resultados para replicar apenas blobs cujos nomes começam com o prefixo especificado.</span><span class="sxs-lookup"><span data-stu-id="5eaa2-120">Filters the results to replicate only blobs whose names begin with the specified prefix.</span></span>

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

### <span data-ttu-id="5eaa2-121">-RuleId</span><span class="sxs-lookup"><span data-stu-id="5eaa2-121">-RuleId</span></span>
<span data-ttu-id="5eaa2-122">ID da Regra de Replicação de Objeto.</span><span class="sxs-lookup"><span data-stu-id="5eaa2-122">Object Replication Rule Id.</span></span>

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

### <span data-ttu-id="5eaa2-123">-SourceContainer</span><span class="sxs-lookup"><span data-stu-id="5eaa2-123">-SourceContainer</span></span>
<span data-ttu-id="5eaa2-124">O nome do Contêiner de origem a ser replicado.</span><span class="sxs-lookup"><span data-stu-id="5eaa2-124">The Source Container name to replicate from.</span></span>

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

### <span data-ttu-id="5eaa2-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5eaa2-125">CommonParameters</span></span>
<span data-ttu-id="5eaa2-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5eaa2-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5eaa2-127">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5eaa2-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5eaa2-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5eaa2-128">INPUTS</span></span>

### <span data-ttu-id="5eaa2-129">Nenhum</span><span class="sxs-lookup"><span data-stu-id="5eaa2-129">None</span></span>

## <span data-ttu-id="5eaa2-130">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="5eaa2-130">OUTPUTS</span></span>

### <span data-ttu-id="5eaa2-131">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicyRule</span><span class="sxs-lookup"><span data-stu-id="5eaa2-131">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicyRule</span></span>

## <span data-ttu-id="5eaa2-132">NOTES</span><span class="sxs-lookup"><span data-stu-id="5eaa2-132">NOTES</span></span>

## <span data-ttu-id="5eaa2-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5eaa2-133">RELATED LINKS</span></span>
