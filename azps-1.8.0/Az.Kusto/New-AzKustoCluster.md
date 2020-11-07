---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/New-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/New-AzKustoCluster.md
ms.openlocfilehash: 9157c5dfff46893cfee88d02d8f1564801f889fe
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93770571"
---
# <span data-ttu-id="646db-101">New-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="646db-101">New-AzKustoCluster</span></span>

## <span data-ttu-id="646db-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="646db-102">SYNOPSIS</span></span>
<span data-ttu-id="646db-103">Cria um novo cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="646db-103">Creates a new Kusto cluster.</span></span>

## <span data-ttu-id="646db-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="646db-104">SYNTAX</span></span>

```
New-AzKustoCluster [-ResourceGroupName] <String> [-Name] <String> -Location <String> -Sku <String>
 [-Tier <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="646db-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="646db-105">DESCRIPTION</span></span>
<span data-ttu-id="646db-106">Cria um novo cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="646db-106">Creates a new Kusto cluster.</span></span>

## <span data-ttu-id="646db-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="646db-107">EXAMPLES</span></span>

### <span data-ttu-id="646db-108">Exemplo 1-criar um novo cluster Kusto</span><span class="sxs-lookup"><span data-stu-id="646db-108">Example 1 - Create a new Kusto cluster</span></span>

```
PS C:\> New-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster -Location 'Central US' -Sku D13_v2 -Capacity 10

Type              : Microsoft.Kusto/Clusters
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster
ResourceGroup     : testrg
Name              : mykustocluster
Location          : Central US
Capacity          : 10
Sku               : D13_v2
ProvisioningState : Succeeded
State             : Running
Tag               : {}
Uri               : https://mykustocluster.centralus.kusto.windows.net
DataIngestionUri  : https://ingest-mykustocluster.centralus.kusto.windows.net
```

<span data-ttu-id="646db-109">O comando acima cria um novo Kusto cluster chamado "mykustocluster" no grupo de recursos "testrg".</span><span class="sxs-lookup"><span data-stu-id="646db-109">The above command creates a new Kusto cluster named "mykustocluster" in the resource group "testrg".</span></span>

## <span data-ttu-id="646db-110">OS</span><span class="sxs-lookup"><span data-stu-id="646db-110">PARAMETERS</span></span>

### <span data-ttu-id="646db-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="646db-111">-DefaultProfile</span></span>
<span data-ttu-id="646db-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="646db-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="646db-113">-Local</span><span class="sxs-lookup"><span data-stu-id="646db-113">-Location</span></span>
<span data-ttu-id="646db-114">Região do Azure em que o cluster deve ser criado.</span><span class="sxs-lookup"><span data-stu-id="646db-114">Azure region where the cluster should be created.</span></span>

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

### <span data-ttu-id="646db-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="646db-115">-Name</span></span>
<span data-ttu-id="646db-116">Nome do cluster a ser criado.</span><span class="sxs-lookup"><span data-stu-id="646db-116">Name of the cluster to be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="646db-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="646db-117">-ResourceGroupName</span></span>
<span data-ttu-id="646db-118">Nome do grupo de recursos sob o qual você deseja criar o cluster.</span><span class="sxs-lookup"><span data-stu-id="646db-118">Name of resource group under which you want to create the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="646db-119">-SKU</span><span class="sxs-lookup"><span data-stu-id="646db-119">-Sku</span></span>
<span data-ttu-id="646db-120">Nome do SKU usado para criar o cluster</span><span class="sxs-lookup"><span data-stu-id="646db-120">Name of the Sku used to create the cluster</span></span>

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

### <span data-ttu-id="646db-121">-Marca</span><span class="sxs-lookup"><span data-stu-id="646db-121">-Tag</span></span>
<span data-ttu-id="646db-122">Uma cadeia de caracteres, dicionário de cadeias de caracteres de marcas associadas a este cluster</span><span class="sxs-lookup"><span data-stu-id="646db-122">A string,string dictionary of tags associated with this cluster</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="646db-123">-Tier</span><span class="sxs-lookup"><span data-stu-id="646db-123">-Tier</span></span>
<span data-ttu-id="646db-124">Nome da camada usada para criar o cluster</span><span class="sxs-lookup"><span data-stu-id="646db-124">Name of the Tier used to create the cluster</span></span>

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

### <span data-ttu-id="646db-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="646db-125">-Confirm</span></span>
<span data-ttu-id="646db-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="646db-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="646db-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="646db-127">-WhatIf</span></span>
<span data-ttu-id="646db-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="646db-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="646db-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="646db-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="646db-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="646db-130">CommonParameters</span></span>
<span data-ttu-id="646db-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="646db-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="646db-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="646db-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="646db-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="646db-133">INPUTS</span></span>

### <span data-ttu-id="646db-134">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="646db-134">None</span></span>

## <span data-ttu-id="646db-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="646db-135">OUTPUTS</span></span>

### <span data-ttu-id="646db-136">Microsoft. Azure. Commands. Kusto. Models. PSKustoCluster</span><span class="sxs-lookup"><span data-stu-id="646db-136">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span></span>

## <span data-ttu-id="646db-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="646db-137">NOTES</span></span>

## <span data-ttu-id="646db-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="646db-138">RELATED LINKS</span></span>
