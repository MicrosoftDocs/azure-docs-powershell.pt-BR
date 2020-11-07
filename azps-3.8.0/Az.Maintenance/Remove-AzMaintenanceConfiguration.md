---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/remove-azmaintenanceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Remove-AzMaintenanceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Remove-AzMaintenanceConfiguration.md
ms.openlocfilehash: 5f212240eaee9ebc46fd7d5cde2ee2e2ec311ac2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944213"
---
# <span data-ttu-id="b128c-101">Remove-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="b128c-101">Remove-AzMaintenanceConfiguration</span></span>

## <span data-ttu-id="b128c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b128c-102">SYNOPSIS</span></span>
<span data-ttu-id="b128c-103">Excluir registro de configuração</span><span class="sxs-lookup"><span data-stu-id="b128c-103">Delete Configuration record</span></span>

## <span data-ttu-id="b128c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b128c-104">SYNTAX</span></span>

```
Remove-AzMaintenanceConfiguration [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b128c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b128c-105">DESCRIPTION</span></span>
<span data-ttu-id="b128c-106">Excluir registro de configuração de manutenção</span><span class="sxs-lookup"><span data-stu-id="b128c-106">Delete Maintenance Configuration record</span></span>

## <span data-ttu-id="b128c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b128c-107">EXAMPLES</span></span>

### <span data-ttu-id="b128c-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b128c-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzMaintenanceConfiguration -ResourceGroupName smdtest -Name workervmscentralus

Remove-AzMaintenanceConfiguration operation
This cmdlet will remove the specified resource.  Do you want to continue?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"):
```

<span data-ttu-id="b128c-109">Excluir registro de configuração de manutenção</span><span class="sxs-lookup"><span data-stu-id="b128c-109">Delete Maintenance Configuration record</span></span>

## <span data-ttu-id="b128c-110">OS</span><span class="sxs-lookup"><span data-stu-id="b128c-110">PARAMETERS</span></span>

### <span data-ttu-id="b128c-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b128c-111">-AsJob</span></span>
<span data-ttu-id="b128c-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="b128c-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b128c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b128c-113">-DefaultProfile</span></span>
<span data-ttu-id="b128c-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b128c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b128c-115">-Force</span><span class="sxs-lookup"><span data-stu-id="b128c-115">-Force</span></span>
<span data-ttu-id="b128c-116">Force remover sem confirmação.</span><span class="sxs-lookup"><span data-stu-id="b128c-116">Force remove without confirmation.</span></span>

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

### <span data-ttu-id="b128c-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="b128c-117">-Name</span></span>
<span data-ttu-id="b128c-118">O nome da configuração de manutenção.</span><span class="sxs-lookup"><span data-stu-id="b128c-118">The maintenance configuration Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b128c-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b128c-119">-PassThru</span></span>
<span data-ttu-id="b128c-120">Retorna o status da operação de remoção.</span><span class="sxs-lookup"><span data-stu-id="b128c-120">Returns the status of the Remove operation.</span></span> <span data-ttu-id="b128c-121">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="b128c-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b128c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b128c-122">-ResourceGroupName</span></span>
<span data-ttu-id="b128c-123">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b128c-123">The resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b128c-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b128c-124">-Confirm</span></span>
<span data-ttu-id="b128c-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b128c-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b128c-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b128c-126">-WhatIf</span></span>
<span data-ttu-id="b128c-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b128c-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b128c-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b128c-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b128c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b128c-129">CommonParameters</span></span>
<span data-ttu-id="b128c-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b128c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b128c-131">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b128c-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b128c-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b128c-132">INPUTS</span></span>

### <span data-ttu-id="b128c-133">System. String</span><span class="sxs-lookup"><span data-stu-id="b128c-133">System.String</span></span>

## <span data-ttu-id="b128c-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b128c-134">OUTPUTS</span></span>

### <span data-ttu-id="b128c-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b128c-135">System.Boolean</span></span>

## <span data-ttu-id="b128c-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b128c-136">NOTES</span></span>

## <span data-ttu-id="b128c-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b128c-137">RELATED LINKS</span></span>
