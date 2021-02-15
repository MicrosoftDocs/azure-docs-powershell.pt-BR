---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/start-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Start-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Start-AzHpcCache.md
ms.openlocfilehash: 7465a74db4da777d60e097fe959ef69bed11918c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111863"
---
# <span data-ttu-id="e4d20-101">Start-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="e4d20-101">Start-AzHpcCache</span></span>

## <span data-ttu-id="e4d20-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e4d20-102">SYNOPSIS</span></span>
<span data-ttu-id="e4d20-103">Inicia o cache HPC.</span><span class="sxs-lookup"><span data-stu-id="e4d20-103">Starts HPC cache.</span></span>

## <span data-ttu-id="e4d20-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e4d20-104">SYNTAX</span></span>

### <span data-ttu-id="e4d20-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e4d20-105">ByFieldsParameterSet (Default)</span></span>
```
Start-AzHpcCache -ResourceGroupName <String> -Name <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4d20-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4d20-106">ByResourceIdParameterSet</span></span>
```
Start-AzHpcCache -ResourceId <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4d20-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4d20-107">ByObjectParameterSet</span></span>
```
Start-AzHpcCache -InputObject <PSHPCCache> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4d20-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="e4d20-108">DESCRIPTION</span></span>
<span data-ttu-id="e4d20-109">O cmdlet **Start-AzHpcCache** inicia um Cache HPC do Azure.</span><span class="sxs-lookup"><span data-stu-id="e4d20-109">The **Start-AzHpcCache** cmdlet starts a Azure HPC Cache.</span></span>

## <span data-ttu-id="e4d20-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e4d20-110">EXAMPLES</span></span>

### <span data-ttu-id="e4d20-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e4d20-111">Example 1</span></span>
```powershell
PS C:\> Start-AzHpcCache -ResourceGroupName testRG -CacheName testCache
```

## <span data-ttu-id="e4d20-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e4d20-112">PARAMETERS</span></span>

### <span data-ttu-id="e4d20-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e4d20-113">-AsJob</span></span>
<span data-ttu-id="e4d20-114">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="e4d20-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e4d20-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4d20-115">-DefaultProfile</span></span>
<span data-ttu-id="e4d20-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e4d20-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4d20-117">-Forçar</span><span class="sxs-lookup"><span data-stu-id="e4d20-117">-Force</span></span>
<span data-ttu-id="e4d20-118">Indica que o cmdlet não solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="e4d20-118">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="e4d20-119">Por padrão, esse cmdlet solicita que você confirme que deseja iniciar o cache.</span><span class="sxs-lookup"><span data-stu-id="e4d20-119">By default, this cmdlet prompts you to confirm that you want to start the cache.</span></span>

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

### <span data-ttu-id="e4d20-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e4d20-120">-InputObject</span></span>
<span data-ttu-id="e4d20-121">O objeto de cache para iniciar.</span><span class="sxs-lookup"><span data-stu-id="e4d20-121">The cache object to start.</span></span>

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

### <span data-ttu-id="e4d20-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="e4d20-122">-Name</span></span>
<span data-ttu-id="e4d20-123">Nome do cache.</span><span class="sxs-lookup"><span data-stu-id="e4d20-123">Name of cache.</span></span>

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

### <span data-ttu-id="e4d20-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e4d20-124">-PassThru</span></span>
<span data-ttu-id="e4d20-125">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="e4d20-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e4d20-126">Por padrão, esse cmdlet não gera saída.</span><span class="sxs-lookup"><span data-stu-id="e4d20-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e4d20-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4d20-127">-ResourceGroupName</span></span>
<span data-ttu-id="e4d20-128">Nome do grupo de recursos no qual você deseja iniciar o cache.</span><span class="sxs-lookup"><span data-stu-id="e4d20-128">Name of resource group under which you want to start cache.</span></span>

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

### <span data-ttu-id="e4d20-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e4d20-129">-ResourceId</span></span>
<span data-ttu-id="e4d20-130">A ID do recurso do Cache</span><span class="sxs-lookup"><span data-stu-id="e4d20-130">The resource id of the Cache</span></span>

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

### <span data-ttu-id="e4d20-131">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="e4d20-131">-Confirm</span></span>
<span data-ttu-id="e4d20-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4d20-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4d20-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4d20-133">-WhatIf</span></span>
<span data-ttu-id="e4d20-134">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="e4d20-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e4d20-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e4d20-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4d20-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4d20-136">CommonParameters</span></span>
<span data-ttu-id="e4d20-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4d20-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4d20-138">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e4d20-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4d20-139">Entradas</span><span class="sxs-lookup"><span data-stu-id="e4d20-139">INPUTS</span></span>

### <span data-ttu-id="e4d20-140">System.String</span><span class="sxs-lookup"><span data-stu-id="e4d20-140">System.String</span></span>

## <span data-ttu-id="e4d20-141">Saídas</span><span class="sxs-lookup"><span data-stu-id="e4d20-141">OUTPUTS</span></span>

## <span data-ttu-id="e4d20-142">Notas</span><span class="sxs-lookup"><span data-stu-id="e4d20-142">NOTES</span></span>

## <span data-ttu-id="e4d20-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e4d20-143">RELATED LINKS</span></span>
