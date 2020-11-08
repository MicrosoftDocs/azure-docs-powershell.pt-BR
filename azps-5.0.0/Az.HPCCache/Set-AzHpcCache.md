---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/set-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Set-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Set-AzHpcCache.md
ms.openlocfilehash: 909f3be2e4a08ff1d1b0538b451ffa93f368d211
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94117394"
---
# <span data-ttu-id="708dd-101">Set-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="708dd-101">Set-AzHpcCache</span></span>

## <span data-ttu-id="708dd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="708dd-102">SYNOPSIS</span></span>
<span data-ttu-id="708dd-103">Atualiza as marcas em um cache HPC.</span><span class="sxs-lookup"><span data-stu-id="708dd-103">Updates tags on a HPC Cache.</span></span>

## <span data-ttu-id="708dd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="708dd-104">SYNTAX</span></span>

### <span data-ttu-id="708dd-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="708dd-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzHpcCache -ResourceGroupName <String> -Name <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="708dd-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="708dd-106">ByObjectParameterSet</span></span>
```
Set-AzHpcCache -InputObject <PSHPCCache> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="708dd-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="708dd-107">DESCRIPTION</span></span>
<span data-ttu-id="708dd-108">O cmdlet **set-AzHpcCache** atualiza as marcas de cache do Azure HPC.</span><span class="sxs-lookup"><span data-stu-id="708dd-108">The **Set-AzHpcCache** cmdlet updates an Azure HPC Cache tags.</span></span>

## <span data-ttu-id="708dd-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="708dd-109">EXAMPLES</span></span>

### <span data-ttu-id="708dd-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="708dd-110">Example 1</span></span>
```powershell
PS C:\> Set-AzHpcCache -ResourceGroupName testRG -CacheName testCache -Tag @{"tag3" = "value1"; "tag4" = "value2"}
```

## <span data-ttu-id="708dd-111">OS</span><span class="sxs-lookup"><span data-stu-id="708dd-111">PARAMETERS</span></span>

### <span data-ttu-id="708dd-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="708dd-112">-AsJob</span></span>
<span data-ttu-id="708dd-113">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="708dd-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="708dd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="708dd-114">-DefaultProfile</span></span>
<span data-ttu-id="708dd-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="708dd-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="708dd-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="708dd-116">-InputObject</span></span>
<span data-ttu-id="708dd-117">O objeto de cache para atualizar.</span><span class="sxs-lookup"><span data-stu-id="708dd-117">The cache object to update.</span></span>

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

### <span data-ttu-id="708dd-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="708dd-118">-Name</span></span>
<span data-ttu-id="708dd-119">Nome do cache.</span><span class="sxs-lookup"><span data-stu-id="708dd-119">Name of cache.</span></span>

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

### <span data-ttu-id="708dd-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="708dd-120">-ResourceGroupName</span></span>
<span data-ttu-id="708dd-121">Nome do grupo de recursos sob o qual você deseja atualizar o cache.</span><span class="sxs-lookup"><span data-stu-id="708dd-121">Name of resource group under which you want to update cache.</span></span>

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

### <span data-ttu-id="708dd-122">-Marca</span><span class="sxs-lookup"><span data-stu-id="708dd-122">-Tag</span></span>
<span data-ttu-id="708dd-123">As marcas a serem associadas ao cache do HPC.</span><span class="sxs-lookup"><span data-stu-id="708dd-123">The tags to associate with HPC Cache.</span></span> 

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

### <span data-ttu-id="708dd-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="708dd-124">-Confirm</span></span>
<span data-ttu-id="708dd-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="708dd-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="708dd-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="708dd-126">-WhatIf</span></span>
<span data-ttu-id="708dd-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="708dd-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="708dd-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="708dd-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="708dd-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="708dd-129">CommonParameters</span></span>
<span data-ttu-id="708dd-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="708dd-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="708dd-131">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="708dd-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="708dd-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="708dd-132">INPUTS</span></span>

### <span data-ttu-id="708dd-133">System. String</span><span class="sxs-lookup"><span data-stu-id="708dd-133">System.String</span></span>

### <span data-ttu-id="708dd-134">System. Int32</span><span class="sxs-lookup"><span data-stu-id="708dd-134">System.Int32</span></span>

## <span data-ttu-id="708dd-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="708dd-135">OUTPUTS</span></span>

### <span data-ttu-id="708dd-136">Microsoft. Azure. PowerShell. cmdlets. HPCCache. Models. PSHPCCache</span><span class="sxs-lookup"><span data-stu-id="708dd-136">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache</span></span>

## <span data-ttu-id="708dd-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="708dd-137">NOTES</span></span>

## <span data-ttu-id="708dd-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="708dd-138">RELATED LINKS</span></span>
