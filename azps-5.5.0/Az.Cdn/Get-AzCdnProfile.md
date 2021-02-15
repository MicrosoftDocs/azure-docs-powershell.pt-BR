---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 28DECA86-37A5-48BE-9727-0C1A3B867E9B
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfile.md
ms.openlocfilehash: 1af77b3fec469b9bb60d5531c89534d5de11b4f0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112180"
---
# <span data-ttu-id="9f07b-101">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="9f07b-101">Get-AzCdnProfile</span></span>

## <span data-ttu-id="9f07b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9f07b-102">SYNOPSIS</span></span>
<span data-ttu-id="9f07b-103">Obtém um perfil de CDN.</span><span class="sxs-lookup"><span data-stu-id="9f07b-103">Gets a CDN profile.</span></span>

## <span data-ttu-id="9f07b-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9f07b-104">SYNTAX</span></span>

```
Get-AzCdnProfile [-ProfileName <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f07b-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="9f07b-105">DESCRIPTION</span></span>
<span data-ttu-id="9f07b-106">O cmdlet **Get-AzCdnProfile** obtém um perfil de Rede de Distribuição de Conteúdo (CDN) do Azure e suas informações relacionadas.</span><span class="sxs-lookup"><span data-stu-id="9f07b-106">The **Get-AzCdnProfile** cmdlet gets an Azure Content Delivery Network (CDN) profile and its related information.</span></span>

## <span data-ttu-id="9f07b-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9f07b-107">EXAMPLES</span></span>

## <span data-ttu-id="9f07b-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9f07b-108">PARAMETERS</span></span>

### <span data-ttu-id="9f07b-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f07b-109">-DefaultProfile</span></span>
<span data-ttu-id="9f07b-110">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="9f07b-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9f07b-111">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="9f07b-111">-ProfileName</span></span>
<span data-ttu-id="9f07b-112">Especifica o nome do perfil.</span><span class="sxs-lookup"><span data-stu-id="9f07b-112">Specifies the name of the profile.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f07b-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f07b-113">-ResourceGroupName</span></span>
<span data-ttu-id="9f07b-114">Especifica o nome do grupo de recursos ao qual o perfil pertence.</span><span class="sxs-lookup"><span data-stu-id="9f07b-114">Specifies the name of the resource group to which the profile belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f07b-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f07b-115">CommonParameters</span></span>
<span data-ttu-id="9f07b-116">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f07b-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f07b-117">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9f07b-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f07b-118">Entradas</span><span class="sxs-lookup"><span data-stu-id="9f07b-118">INPUTS</span></span>

### <span data-ttu-id="9f07b-119">System.String</span><span class="sxs-lookup"><span data-stu-id="9f07b-119">System.String</span></span>

## <span data-ttu-id="9f07b-120">Saídas</span><span class="sxs-lookup"><span data-stu-id="9f07b-120">OUTPUTS</span></span>

### <span data-ttu-id="9f07b-121">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="9f07b-121">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="9f07b-122">Notas</span><span class="sxs-lookup"><span data-stu-id="9f07b-122">NOTES</span></span>

## <span data-ttu-id="9f07b-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9f07b-123">RELATED LINKS</span></span>

[<span data-ttu-id="9f07b-124">Novo-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="9f07b-124">New-AzCdnProfile</span></span>](./New-AzCdnProfile.md)

[<span data-ttu-id="9f07b-125">Remove-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="9f07b-125">Remove-AzCdnProfile</span></span>](./Remove-AzCdnProfile.md)

[<span data-ttu-id="9f07b-126">Set-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="9f07b-126">Set-AzCdnProfile</span></span>](./Set-AzCdnProfile.md)


