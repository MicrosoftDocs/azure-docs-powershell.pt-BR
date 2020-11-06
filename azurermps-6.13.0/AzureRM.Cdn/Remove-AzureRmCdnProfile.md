---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 3A4F8442-1268-44BC-91ED-47C03CD20C47
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/remove-azurermcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnProfile.md
ms.openlocfilehash: 0c39e6ee26faffc9c12e2fc3b5f00ccaadfa9389
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431385"
---
# <span data-ttu-id="0f9a6-101">Remove-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="0f9a6-101">Remove-AzureRmCdnProfile</span></span>

## <span data-ttu-id="0f9a6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0f9a6-102">SYNOPSIS</span></span>
<span data-ttu-id="0f9a6-103">Remove um perfil CDN.</span><span class="sxs-lookup"><span data-stu-id="0f9a6-103">Removes a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0f9a6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0f9a6-104">SYNTAX</span></span>

### <span data-ttu-id="0f9a6-105">ByFieldsParameterSet</span><span class="sxs-lookup"><span data-stu-id="0f9a6-105">ByFieldsParameterSet</span></span>
```
Remove-AzureRmCdnProfile -ProfileName <String> -ResourceGroupName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f9a6-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0f9a6-106">ByObjectParameterSet</span></span>
```
Remove-AzureRmCdnProfile -CdnProfile <PSProfile> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f9a6-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0f9a6-107">DESCRIPTION</span></span>
<span data-ttu-id="0f9a6-108">O cmdlet **Remove-AzureRmCdnProfile** remove um perfil da CDN (rede de distribuição de conteúdo) do Azure.</span><span class="sxs-lookup"><span data-stu-id="0f9a6-108">The **Remove-AzureRmCdnProfile** cmdlet removes a Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="0f9a6-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0f9a6-109">EXAMPLES</span></span>

## <span data-ttu-id="0f9a6-110">OS</span><span class="sxs-lookup"><span data-stu-id="0f9a6-110">PARAMETERS</span></span>

### <span data-ttu-id="0f9a6-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="0f9a6-111">-CdnProfile</span></span>
<span data-ttu-id="0f9a6-112">Especifica o perfil que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="0f9a6-112">Specifies the profile that this cmdlet removes.</span></span>

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

### <span data-ttu-id="0f9a6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f9a6-113">-DefaultProfile</span></span>
<span data-ttu-id="0f9a6-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="0f9a6-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f9a6-115">-Force</span><span class="sxs-lookup"><span data-stu-id="0f9a6-115">-Force</span></span>
<span data-ttu-id="0f9a6-116">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="0f9a6-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0f9a6-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0f9a6-117">-PassThru</span></span>
<span data-ttu-id="0f9a6-118">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="0f9a6-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0f9a6-119">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="0f9a6-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0f9a6-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="0f9a6-120">-ProfileName</span></span>
<span data-ttu-id="0f9a6-121">Especifica o nome do perfil que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="0f9a6-121">Specifies the name of the profile that this cmdlet removes.</span></span>

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

### <span data-ttu-id="0f9a6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f9a6-122">-ResourceGroupName</span></span>
<span data-ttu-id="0f9a6-123">Especifica o nome do grupo de recursos ao qual o perfil pertence.</span><span class="sxs-lookup"><span data-stu-id="0f9a6-123">Specifies the name of the resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="0f9a6-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0f9a6-124">-Confirm</span></span>
<span data-ttu-id="0f9a6-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0f9a6-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f9a6-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f9a6-126">-WhatIf</span></span>
<span data-ttu-id="0f9a6-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0f9a6-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f9a6-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0f9a6-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f9a6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f9a6-129">CommonParameters</span></span>
<span data-ttu-id="0f9a6-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f9a6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f9a6-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f9a6-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f9a6-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0f9a6-132">INPUTS</span></span>

### <span data-ttu-id="0f9a6-133">Microsoft. Azure. Commands. cdn. Models. Profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="0f9a6-133">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>
<span data-ttu-id="0f9a6-134">Parâmetros: CdnProfile (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0f9a6-134">Parameters: CdnProfile (ByValue)</span></span>

### <span data-ttu-id="0f9a6-135">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="0f9a6-135">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="0f9a6-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0f9a6-136">OUTPUTS</span></span>

### <span data-ttu-id="0f9a6-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0f9a6-137">System.Boolean</span></span>

## <span data-ttu-id="0f9a6-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0f9a6-138">NOTES</span></span>

## <span data-ttu-id="0f9a6-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0f9a6-139">RELATED LINKS</span></span>

[<span data-ttu-id="0f9a6-140">Get-AzureRMCdnProfile</span><span class="sxs-lookup"><span data-stu-id="0f9a6-140">Get-AzureRMCdnProfile</span></span>](./Get-AzureRMCdnProfile.md)

[<span data-ttu-id="0f9a6-141">New-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="0f9a6-141">New-AzureRmCdnProfile</span></span>](./New-AzureRmCdnProfile.md)

[<span data-ttu-id="0f9a6-142">Set-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="0f9a6-142">Set-AzureRmCdnProfile</span></span>](./Set-AzureRmCdnProfile.md)


