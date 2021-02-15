---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/set-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Set-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Set-AzHpcCache.md
ms.openlocfilehash: 909f3be2e4a08ff1d1b0538b451ffa93f368d211
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118974"
---
# <span data-ttu-id="0e5db-101">Set-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="0e5db-101">Set-AzHpcCache</span></span>

## <span data-ttu-id="0e5db-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0e5db-102">SYNOPSIS</span></span>
<span data-ttu-id="0e5db-103">Atualiza marcas em um Cache HPC.</span><span class="sxs-lookup"><span data-stu-id="0e5db-103">Updates tags on a HPC Cache.</span></span>

## <span data-ttu-id="0e5db-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0e5db-104">SYNTAX</span></span>

### <span data-ttu-id="0e5db-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="0e5db-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzHpcCache -ResourceGroupName <String> -Name <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e5db-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0e5db-106">ByObjectParameterSet</span></span>
```
Set-AzHpcCache -InputObject <PSHPCCache> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e5db-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="0e5db-107">DESCRIPTION</span></span>
<span data-ttu-id="0e5db-108">O **cmdlet Set-AzHpcCache** atualiza uma marca de Cache HPC do Azure.</span><span class="sxs-lookup"><span data-stu-id="0e5db-108">The **Set-AzHpcCache** cmdlet updates an Azure HPC Cache tags.</span></span>

## <span data-ttu-id="0e5db-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0e5db-109">EXAMPLES</span></span>

### <span data-ttu-id="0e5db-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0e5db-110">Example 1</span></span>
```powershell
PS C:\> Set-AzHpcCache -ResourceGroupName testRG -CacheName testCache -Tag @{"tag3" = "value1"; "tag4" = "value2"}
```

## <span data-ttu-id="0e5db-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0e5db-111">PARAMETERS</span></span>

### <span data-ttu-id="0e5db-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0e5db-112">-AsJob</span></span>
<span data-ttu-id="0e5db-113">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="0e5db-113">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e5db-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e5db-114">-DefaultProfile</span></span>
<span data-ttu-id="0e5db-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0e5db-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e5db-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0e5db-116">-InputObject</span></span>
<span data-ttu-id="0e5db-117">O objeto de cache a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="0e5db-117">The cache object to update.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0e5db-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="0e5db-118">-Name</span></span>
<span data-ttu-id="0e5db-119">Nome do cache.</span><span class="sxs-lookup"><span data-stu-id="0e5db-119">Name of cache.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: CacheName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e5db-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e5db-120">-ResourceGroupName</span></span>
<span data-ttu-id="0e5db-121">Nome do grupo de recursos no qual você deseja atualizar o cache.</span><span class="sxs-lookup"><span data-stu-id="0e5db-121">Name of resource group under which you want to update cache.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e5db-122">-Tag</span><span class="sxs-lookup"><span data-stu-id="0e5db-122">-Tag</span></span>
<span data-ttu-id="0e5db-123">As marcas a associar ao Cache HPC.</span><span class="sxs-lookup"><span data-stu-id="0e5db-123">The tags to associate with HPC Cache.</span></span> 

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e5db-124">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="0e5db-124">-Confirm</span></span>
<span data-ttu-id="0e5db-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0e5db-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e5db-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e5db-126">-WhatIf</span></span>
<span data-ttu-id="0e5db-127">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="0e5db-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0e5db-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0e5db-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e5db-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e5db-129">CommonParameters</span></span>
<span data-ttu-id="0e5db-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e5db-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e5db-131">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0e5db-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e5db-132">Entradas</span><span class="sxs-lookup"><span data-stu-id="0e5db-132">INPUTS</span></span>

### <span data-ttu-id="0e5db-133">System.String</span><span class="sxs-lookup"><span data-stu-id="0e5db-133">System.String</span></span>

### <span data-ttu-id="0e5db-134">System.Int32</span><span class="sxs-lookup"><span data-stu-id="0e5db-134">System.Int32</span></span>

## <span data-ttu-id="0e5db-135">Saídas</span><span class="sxs-lookup"><span data-stu-id="0e5db-135">OUTPUTS</span></span>

### <span data-ttu-id="0e5db-136">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache</span><span class="sxs-lookup"><span data-stu-id="0e5db-136">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache</span></span>

## <span data-ttu-id="0e5db-137">Notas</span><span class="sxs-lookup"><span data-stu-id="0e5db-137">NOTES</span></span>

## <span data-ttu-id="0e5db-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0e5db-138">RELATED LINKS</span></span>
