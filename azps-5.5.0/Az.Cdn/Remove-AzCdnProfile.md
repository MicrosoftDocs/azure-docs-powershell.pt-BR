---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 3A4F8442-1268-44BC-91ED-47C03CD20C47
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/remove-azcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnProfile.md
ms.openlocfilehash: ba45ea8d4c1b58290623f7f415f09cdb7663f575
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116579"
---
# <span data-ttu-id="e25d3-101">Remove-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="e25d3-101">Remove-AzCdnProfile</span></span>

## <span data-ttu-id="e25d3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e25d3-102">SYNOPSIS</span></span>
<span data-ttu-id="e25d3-103">Remove um perfil de CDN.</span><span class="sxs-lookup"><span data-stu-id="e25d3-103">Removes a CDN profile.</span></span>

## <span data-ttu-id="e25d3-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e25d3-104">SYNTAX</span></span>

### <span data-ttu-id="e25d3-105">ByFieldsParameterSet</span><span class="sxs-lookup"><span data-stu-id="e25d3-105">ByFieldsParameterSet</span></span>
```
Remove-AzCdnProfile -ProfileName <String> -ResourceGroupName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e25d3-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e25d3-106">ByObjectParameterSet</span></span>
```
Remove-AzCdnProfile -CdnProfile <PSProfile> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e25d3-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="e25d3-107">DESCRIPTION</span></span>
<span data-ttu-id="e25d3-108">O cmdlet **Remove-AzCdnProfile** remove um perfil de REDE de Distribuição de Conteúdo (CDN) do Azure.</span><span class="sxs-lookup"><span data-stu-id="e25d3-108">The **Remove-AzCdnProfile** cmdlet removes a Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="e25d3-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e25d3-109">EXAMPLES</span></span>

## <span data-ttu-id="e25d3-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e25d3-110">PARAMETERS</span></span>

### <span data-ttu-id="e25d3-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="e25d3-111">-CdnProfile</span></span>
<span data-ttu-id="e25d3-112">Especifica o perfil que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="e25d3-112">Specifies the profile that this cmdlet removes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e25d3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e25d3-113">-DefaultProfile</span></span>
<span data-ttu-id="e25d3-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="e25d3-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e25d3-115">-Forçar</span><span class="sxs-lookup"><span data-stu-id="e25d3-115">-Force</span></span>
<span data-ttu-id="e25d3-116">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="e25d3-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e25d3-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e25d3-117">-PassThru</span></span>
<span data-ttu-id="e25d3-118">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="e25d3-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e25d3-119">Por padrão, esse cmdlet não gera saída.</span><span class="sxs-lookup"><span data-stu-id="e25d3-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e25d3-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="e25d3-120">-ProfileName</span></span>
<span data-ttu-id="e25d3-121">Especifica o nome do perfil que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="e25d3-121">Specifies the name of the profile that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e25d3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e25d3-122">-ResourceGroupName</span></span>
<span data-ttu-id="e25d3-123">Especifica o nome do grupo de recursos ao qual o perfil pertence.</span><span class="sxs-lookup"><span data-stu-id="e25d3-123">Specifies the name of the resource group to which the profile belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e25d3-124">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="e25d3-124">-Confirm</span></span>
<span data-ttu-id="e25d3-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e25d3-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e25d3-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e25d3-126">-WhatIf</span></span>
<span data-ttu-id="e25d3-127">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="e25d3-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e25d3-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e25d3-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e25d3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e25d3-129">CommonParameters</span></span>
<span data-ttu-id="e25d3-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e25d3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e25d3-131">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e25d3-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e25d3-132">Entradas</span><span class="sxs-lookup"><span data-stu-id="e25d3-132">INPUTS</span></span>

### <span data-ttu-id="e25d3-133">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="e25d3-133">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

### <span data-ttu-id="e25d3-134">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e25d3-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e25d3-135">Saídas</span><span class="sxs-lookup"><span data-stu-id="e25d3-135">OUTPUTS</span></span>

### <span data-ttu-id="e25d3-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e25d3-136">System.Boolean</span></span>

## <span data-ttu-id="e25d3-137">Notas</span><span class="sxs-lookup"><span data-stu-id="e25d3-137">NOTES</span></span>

## <span data-ttu-id="e25d3-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e25d3-138">RELATED LINKS</span></span>

[<span data-ttu-id="e25d3-139">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="e25d3-139">Get-AzCdnProfile</span></span>](./Get-AzCdnProfile.md)

[<span data-ttu-id="e25d3-140">Novo-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="e25d3-140">New-AzCdnProfile</span></span>](./New-AzCdnProfile.md)

[<span data-ttu-id="e25d3-141">Set-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="e25d3-141">Set-AzCdnProfile</span></span>](./Set-AzCdnProfile.md)


