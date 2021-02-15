---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/New-azstorageobjectreplicationpolicyrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageObjectReplicationPolicyRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageObjectReplicationPolicyRule.md
ms.openlocfilehash: c8d41300250e41548cf949248b02c819b7da497f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114427"
---
# <span data-ttu-id="e811b-101">New-AzStorageObjectReplicationPolicyRule</span><span class="sxs-lookup"><span data-stu-id="e811b-101">New-AzStorageObjectReplicationPolicyRule</span></span>

## <span data-ttu-id="e811b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e811b-102">SYNOPSIS</span></span>
<span data-ttu-id="e811b-103">Cria uma regra de política de replicação de objeto.</span><span class="sxs-lookup"><span data-stu-id="e811b-103">Creates an object replication policy rule.</span></span>

## <span data-ttu-id="e811b-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e811b-104">SYNTAX</span></span>

```
New-AzStorageObjectReplicationPolicyRule -SourceContainer <String> -DestinationContainer <String>
 [-PrefixMatch <String[]>] [-MinCreationTime <DateTime>] [-RuleId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e811b-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="e811b-105">DESCRIPTION</span></span>
<span data-ttu-id="e811b-106">O cmdlet **Get-AzStorageObjectReplicationPolicy** cria uma regra de política de replicação de objeto, que será usada no cmdlet Set-AzStorageObjectReplicationPolicy.</span><span class="sxs-lookup"><span data-stu-id="e811b-106">The **Get-AzStorageObjectReplicationPolicy** cmdlet creates an object replication policy rule, which will be used in Set-AzStorageObjectReplicationPolicy cmdlet.</span></span>

## <span data-ttu-id="e811b-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e811b-107">EXAMPLES</span></span>

### <span data-ttu-id="e811b-108">Exemplo 1: Criar uma regra de política de replicação de objeto com apenas conta de origem e destino e mostrar suas propriedades</span><span class="sxs-lookup"><span data-stu-id="e811b-108">Example 1: Create an object replication policy rule with only source and destination account, and show its properties</span></span>
```
PS C:\> $rule1 = New-AzStorageObjectReplicationPolicyRule -SourceContainer src1 -DestinationContainer dest1 

PS C:\> $rule1

RuleId SourceContainer DestinationContainer Filters.PrefixMatch Filters.MinCreationTime
------ --------------- -------------------- ------------------- -----------------------
       src1            dest1                {}
```

<span data-ttu-id="e811b-109">Esse comando cria uma regra de política de replicação de objeto com apenas conta de origem e destino e mostra suas propriedades.</span><span class="sxs-lookup"><span data-stu-id="e811b-109">This command creates an object replication policy rule with only source and destination account, and show its properties.</span></span>

### <span data-ttu-id="e811b-110">Exemplo 2: Criar uma regra de política de replicação de objeto com todas as propriedades e mostrar suas propriedades</span><span class="sxs-lookup"><span data-stu-id="e811b-110">Example 2: Create an object replication policy rule with all properties, and show its properties</span></span>
```
PS C:\> $rule2 = New-AzStorageObjectReplicationPolicyRule -SourceContainer src -DestinationContainer dest -MinCreationTime 2019-01-01T16:00:00Z -PrefixMatch a,abc,dd

PS C:\> $rule2

RuleId SourceContainer DestinationContainer Filters.PrefixMatch Filters.MinCreationTime
------ --------------- -------------------- ------------------- -----------------------
       src             dest                 {a, abc, dd}        2019-01-01T16:00:00Z
```

<span data-ttu-id="e811b-111">Esse comando é uma regra de política de replicação de objeto com todas as propriedades e mostra suas propriedades.</span><span class="sxs-lookup"><span data-stu-id="e811b-111">This command an object replication policy rule with all properties, and show its properties.</span></span>

## <span data-ttu-id="e811b-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e811b-112">PARAMETERS</span></span>

### <span data-ttu-id="e811b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e811b-113">-DefaultProfile</span></span>
<span data-ttu-id="e811b-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e811b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e811b-115">-DestinationContainer</span><span class="sxs-lookup"><span data-stu-id="e811b-115">-DestinationContainer</span></span>
<span data-ttu-id="e811b-116">O nome do Contêiner de Destino para o que se replicar.</span><span class="sxs-lookup"><span data-stu-id="e811b-116">The Destination Container name to replicate to.</span></span>

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

### <span data-ttu-id="e811b-117">-MinCreationTime</span><span class="sxs-lookup"><span data-stu-id="e811b-117">-MinCreationTime</span></span>
<span data-ttu-id="e811b-118">Os blobs criados após o horário serão replicados para o destino..</span><span class="sxs-lookup"><span data-stu-id="e811b-118">Blobs created after the time will be replicated to the destination..</span></span>

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

### <span data-ttu-id="e811b-119">-PrefixMatch</span><span class="sxs-lookup"><span data-stu-id="e811b-119">-PrefixMatch</span></span>
<span data-ttu-id="e811b-120">Filtra os resultados para replicar somente blobs cujos nomes começam com o prefixo especificado.</span><span class="sxs-lookup"><span data-stu-id="e811b-120">Filters the results to replicate only blobs whose names begin with the specified prefix.</span></span>

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

### <span data-ttu-id="e811b-121">-RuleId</span><span class="sxs-lookup"><span data-stu-id="e811b-121">-RuleId</span></span>
<span data-ttu-id="e811b-122">ID da Regra de Replicação de Objeto.</span><span class="sxs-lookup"><span data-stu-id="e811b-122">Object Replication Rule Id.</span></span>

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

### <span data-ttu-id="e811b-123">-SourceContainer</span><span class="sxs-lookup"><span data-stu-id="e811b-123">-SourceContainer</span></span>
<span data-ttu-id="e811b-124">O nome do Contêiner de Origem a ser replicado.</span><span class="sxs-lookup"><span data-stu-id="e811b-124">The Source Container name to replicate from.</span></span>

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

### <span data-ttu-id="e811b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e811b-125">CommonParameters</span></span>
<span data-ttu-id="e811b-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e811b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e811b-127">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e811b-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e811b-128">Entradas</span><span class="sxs-lookup"><span data-stu-id="e811b-128">INPUTS</span></span>

### <span data-ttu-id="e811b-129">Nenhum</span><span class="sxs-lookup"><span data-stu-id="e811b-129">None</span></span>

## <span data-ttu-id="e811b-130">Saídas</span><span class="sxs-lookup"><span data-stu-id="e811b-130">OUTPUTS</span></span>

### <span data-ttu-id="e811b-131">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicyRule</span><span class="sxs-lookup"><span data-stu-id="e811b-131">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicyRule</span></span>

## <span data-ttu-id="e811b-132">Notas</span><span class="sxs-lookup"><span data-stu-id="e811b-132">NOTES</span></span>

## <span data-ttu-id="e811b-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e811b-133">RELATED LINKS</span></span>
