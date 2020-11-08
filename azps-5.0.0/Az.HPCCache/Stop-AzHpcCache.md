---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/stop-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Stop-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Stop-AzHpcCache.md
ms.openlocfilehash: 22813d762fe575f7f34b6c8eb81f1b5c1c167047
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94115349"
---
# <span data-ttu-id="1acc7-101">Stop-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="1acc7-101">Stop-AzHpcCache</span></span>

## <span data-ttu-id="1acc7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1acc7-102">SYNOPSIS</span></span>
<span data-ttu-id="1acc7-103">Interrompe o cache do HPC.</span><span class="sxs-lookup"><span data-stu-id="1acc7-103">Stops HPC cache.</span></span>

## <span data-ttu-id="1acc7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1acc7-104">SYNTAX</span></span>

### <span data-ttu-id="1acc7-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="1acc7-105">ByFieldsParameterSet (Default)</span></span>
```
Stop-AzHpcCache -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1acc7-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1acc7-106">ByResourceIdParameterSet</span></span>
```
Stop-AzHpcCache -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1acc7-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1acc7-107">ByObjectParameterSet</span></span>
```
Stop-AzHpcCache -InputObject <PSHPCCache> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1acc7-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1acc7-108">DESCRIPTION</span></span>
<span data-ttu-id="1acc7-109">O cmdlet **Stop-AzHpcCache** interrompe um cache do Azure HPC.</span><span class="sxs-lookup"><span data-stu-id="1acc7-109">The **Stop-AzHpcCache** cmdlet stops a Azure HPC Cache.</span></span>

## <span data-ttu-id="1acc7-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1acc7-110">EXAMPLES</span></span>

### <span data-ttu-id="1acc7-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1acc7-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzHpcCache -ResourceGroupName testRG -CacheName testCache
```

## <span data-ttu-id="1acc7-112">OS</span><span class="sxs-lookup"><span data-stu-id="1acc7-112">PARAMETERS</span></span>

### <span data-ttu-id="1acc7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1acc7-113">-DefaultProfile</span></span>
<span data-ttu-id="1acc7-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1acc7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1acc7-115">-Force</span><span class="sxs-lookup"><span data-stu-id="1acc7-115">-Force</span></span>
<span data-ttu-id="1acc7-116">Indica que o cmdlet não solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="1acc7-116">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="1acc7-117">Por padrão, esse cmdlet solicita que você confirme se deseja parar o cache.</span><span class="sxs-lookup"><span data-stu-id="1acc7-117">By default, this cmdlet prompts you to confirm that you want to stop the cache.</span></span>

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

### <span data-ttu-id="1acc7-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1acc7-118">-InputObject</span></span>
<span data-ttu-id="1acc7-119">O objeto de cache para parar.</span><span class="sxs-lookup"><span data-stu-id="1acc7-119">The cache object to stop.</span></span>

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

### <span data-ttu-id="1acc7-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="1acc7-120">-Name</span></span>
<span data-ttu-id="1acc7-121">Nome do cache.</span><span class="sxs-lookup"><span data-stu-id="1acc7-121">Name of cache.</span></span>

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

### <span data-ttu-id="1acc7-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1acc7-122">-PassThru</span></span>
<span data-ttu-id="1acc7-123">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="1acc7-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="1acc7-124">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="1acc7-124">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1acc7-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1acc7-125">-ResourceGroupName</span></span>
<span data-ttu-id="1acc7-126">Nome do grupo de recursos sob o qual você deseja parar o cache.</span><span class="sxs-lookup"><span data-stu-id="1acc7-126">Name of resource group under which you want to stop cache.</span></span>

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

### <span data-ttu-id="1acc7-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1acc7-127">-ResourceId</span></span>
<span data-ttu-id="1acc7-128">A ID do recurso do cache</span><span class="sxs-lookup"><span data-stu-id="1acc7-128">The resource id of the Cache</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1acc7-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1acc7-129">-Confirm</span></span>
<span data-ttu-id="1acc7-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1acc7-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1acc7-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1acc7-131">-WhatIf</span></span>
<span data-ttu-id="1acc7-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1acc7-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1acc7-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1acc7-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1acc7-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1acc7-134">CommonParameters</span></span>
<span data-ttu-id="1acc7-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1acc7-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1acc7-136">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1acc7-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1acc7-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1acc7-137">INPUTS</span></span>

### <span data-ttu-id="1acc7-138">System. String</span><span class="sxs-lookup"><span data-stu-id="1acc7-138">System.String</span></span>

## <span data-ttu-id="1acc7-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1acc7-139">OUTPUTS</span></span>

## <span data-ttu-id="1acc7-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1acc7-140">NOTES</span></span>

## <span data-ttu-id="1acc7-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1acc7-141">RELATED LINKS</span></span>
