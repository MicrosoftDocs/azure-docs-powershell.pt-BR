---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 3A4F8442-1268-44BC-91ED-47C03CD20C47
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnProfile.md
ms.openlocfilehash: f564a026359042a20e5d82e34425e98f1021422b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431133"
---
# <span data-ttu-id="e4835-101">Remove-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="e4835-101">Remove-AzureRmCdnProfile</span></span>

## <span data-ttu-id="e4835-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e4835-102">SYNOPSIS</span></span>
<span data-ttu-id="e4835-103">Remove um perfil CDN.</span><span class="sxs-lookup"><span data-stu-id="e4835-103">Removes a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e4835-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e4835-104">SYNTAX</span></span>

### <span data-ttu-id="e4835-105">Conjunto de parâmetros para parâmetros de campos</span><span class="sxs-lookup"><span data-stu-id="e4835-105">Parameter Set for fields parameters</span></span>
```
Remove-AzureRmCdnProfile -ProfileName <String> -ResourceGroupName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4835-106">Conjunto de parâmetros para parâmetros de objeto</span><span class="sxs-lookup"><span data-stu-id="e4835-106">Parameter Set for object parameters</span></span>
```
Remove-AzureRmCdnProfile -CdnProfile <PSProfile> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4835-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e4835-107">DESCRIPTION</span></span>
<span data-ttu-id="e4835-108">O cmdlet **Remove-AzureRmCdnProfile** remove um perfil da CDN (rede de distribuição de conteúdo) do Azure.</span><span class="sxs-lookup"><span data-stu-id="e4835-108">The **Remove-AzureRmCdnProfile** cmdlet removes a Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="e4835-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e4835-109">EXAMPLES</span></span>

## <span data-ttu-id="e4835-110">OS</span><span class="sxs-lookup"><span data-stu-id="e4835-110">PARAMETERS</span></span>

### <span data-ttu-id="e4835-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="e4835-111">-CdnProfile</span></span>
<span data-ttu-id="e4835-112">Especifica o perfil que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="e4835-112">Specifies the profile that this cmdlet removes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: Parameter Set for object parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e4835-113">-Force</span><span class="sxs-lookup"><span data-stu-id="e4835-113">-Force</span></span>
<span data-ttu-id="e4835-114">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="e4835-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e4835-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e4835-115">-PassThru</span></span>
<span data-ttu-id="e4835-116">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="e4835-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e4835-117">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="e4835-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e4835-118">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="e4835-118">-ProfileName</span></span>
<span data-ttu-id="e4835-119">Especifica o nome do perfil que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="e4835-119">Specifies the name of the profile that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4835-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4835-120">-ResourceGroupName</span></span>
<span data-ttu-id="e4835-121">Especifica o nome do grupo de recursos ao qual o perfil pertence.</span><span class="sxs-lookup"><span data-stu-id="e4835-121">Specifies the name of the resource group to which the profile belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4835-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e4835-122">-Confirm</span></span>
<span data-ttu-id="e4835-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4835-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4835-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4835-124">-WhatIf</span></span>
<span data-ttu-id="e4835-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e4835-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4835-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e4835-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4835-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4835-127">-DefaultProfile</span></span>
<span data-ttu-id="e4835-128">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e4835-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e4835-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4835-129">CommonParameters</span></span>
<span data-ttu-id="e4835-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4835-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4835-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4835-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4835-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e4835-132">INPUTS</span></span>

### <span data-ttu-id="e4835-133">PSProfile</span><span class="sxs-lookup"><span data-stu-id="e4835-133">PSProfile</span></span>
<span data-ttu-id="e4835-134">O parâmetro ' CdnProfile ' aceita o valor do tipo ' PSProfile ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="e4835-134">Parameter 'CdnProfile' accepts value of type 'PSProfile' from the pipeline</span></span>

## <span data-ttu-id="e4835-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e4835-135">OUTPUTS</span></span>

### <span data-ttu-id="e4835-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e4835-136">System.Boolean</span></span>

## <span data-ttu-id="e4835-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e4835-137">NOTES</span></span>

## <span data-ttu-id="e4835-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e4835-138">RELATED LINKS</span></span>

[<span data-ttu-id="e4835-139">Get-AzureRMCdnProfile</span><span class="sxs-lookup"><span data-stu-id="e4835-139">Get-AzureRMCdnProfile</span></span>](./Get-AzureRMCdnProfile.md)

[<span data-ttu-id="e4835-140">New-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="e4835-140">New-AzureRmCdnProfile</span></span>](./New-AzureRmCdnProfile.md)

[<span data-ttu-id="e4835-141">Set-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="e4835-141">Set-AzureRmCdnProfile</span></span>](./Set-AzureRmCdnProfile.md)


