---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 3A4F8442-1268-44BC-91ED-47C03CD20C47
online version: https://docs.microsoft.com/powershell/module/az.cdn/remove-azcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnProfile.md
ms.openlocfilehash: 904af1f1d1f6cba7bd0a44ee0811b55fef01e106
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891222"
---
# <span data-ttu-id="5ffb9-101">Remove-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="5ffb9-101">Remove-AzCdnProfile</span></span>

## <span data-ttu-id="5ffb9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ffb9-102">SYNOPSIS</span></span>
<span data-ttu-id="5ffb9-103">Remove um perfil de CDN.</span><span class="sxs-lookup"><span data-stu-id="5ffb9-103">Removes a CDN profile.</span></span>

## <span data-ttu-id="5ffb9-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="5ffb9-104">SYNTAX</span></span>

### <span data-ttu-id="5ffb9-105">ByFieldsParameterSet</span><span class="sxs-lookup"><span data-stu-id="5ffb9-105">ByFieldsParameterSet</span></span>
```
Remove-AzCdnProfile -ProfileName <String> -ResourceGroupName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ffb9-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5ffb9-106">ByObjectParameterSet</span></span>
```
Remove-AzCdnProfile -CdnProfile <PSProfile> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ffb9-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="5ffb9-107">DESCRIPTION</span></span>
<span data-ttu-id="5ffb9-108">O cmdlet **Remove-AzCdnProfile** remove um perfil cdn (Rede de Distribuição de Conteúdo) do Azure.</span><span class="sxs-lookup"><span data-stu-id="5ffb9-108">The **Remove-AzCdnProfile** cmdlet removes a Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="5ffb9-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5ffb9-109">EXAMPLES</span></span>

## <span data-ttu-id="5ffb9-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="5ffb9-110">PARAMETERS</span></span>

### <span data-ttu-id="5ffb9-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="5ffb9-111">-CdnProfile</span></span>
<span data-ttu-id="5ffb9-112">Especifica o perfil que esse cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="5ffb9-112">Specifies the profile that this cmdlet removes.</span></span>

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

### <span data-ttu-id="5ffb9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ffb9-113">-DefaultProfile</span></span>
<span data-ttu-id="5ffb9-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="5ffb9-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5ffb9-115">-Force</span><span class="sxs-lookup"><span data-stu-id="5ffb9-115">-Force</span></span>
<span data-ttu-id="5ffb9-116">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="5ffb9-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5ffb9-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5ffb9-117">-PassThru</span></span>
<span data-ttu-id="5ffb9-118">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="5ffb9-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="5ffb9-119">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="5ffb9-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5ffb9-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="5ffb9-120">-ProfileName</span></span>
<span data-ttu-id="5ffb9-121">Especifica o nome do perfil que esse cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="5ffb9-121">Specifies the name of the profile that this cmdlet removes.</span></span>

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

### <span data-ttu-id="5ffb9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ffb9-122">-ResourceGroupName</span></span>
<span data-ttu-id="5ffb9-123">Especifica o nome do grupo de recursos ao qual o perfil pertence.</span><span class="sxs-lookup"><span data-stu-id="5ffb9-123">Specifies the name of the resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="5ffb9-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5ffb9-124">-Confirm</span></span>
<span data-ttu-id="5ffb9-125">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ffb9-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ffb9-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ffb9-126">-WhatIf</span></span>
<span data-ttu-id="5ffb9-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5ffb9-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ffb9-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5ffb9-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ffb9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ffb9-129">CommonParameters</span></span>
<span data-ttu-id="5ffb9-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ffb9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ffb9-131">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5ffb9-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ffb9-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5ffb9-132">INPUTS</span></span>

### <span data-ttu-id="5ffb9-133">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="5ffb9-133">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

### <span data-ttu-id="5ffb9-134">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="5ffb9-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="5ffb9-135">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="5ffb9-135">OUTPUTS</span></span>

### <span data-ttu-id="5ffb9-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5ffb9-136">System.Boolean</span></span>

## <span data-ttu-id="5ffb9-137">NOTES</span><span class="sxs-lookup"><span data-stu-id="5ffb9-137">NOTES</span></span>

## <span data-ttu-id="5ffb9-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5ffb9-138">RELATED LINKS</span></span>

[<span data-ttu-id="5ffb9-139">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="5ffb9-139">Get-AzCdnProfile</span></span>](./Get-AzCdnProfile.md)

[<span data-ttu-id="5ffb9-140">New-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="5ffb9-140">New-AzCdnProfile</span></span>](./New-AzCdnProfile.md)

[<span data-ttu-id="5ffb9-141">Set-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="5ffb9-141">Set-AzCdnProfile</span></span>](./Set-AzCdnProfile.md)


