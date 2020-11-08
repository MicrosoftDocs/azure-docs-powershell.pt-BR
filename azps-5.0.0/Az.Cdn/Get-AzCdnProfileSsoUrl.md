---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 93D5E2D9-FB89-4311-8E8E-44CBFAFC98A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnprofilessourl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSsoUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSsoUrl.md
ms.openlocfilehash: 74bc4fae4dd55a85c4aca811819a0348f5df5f2c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94125467"
---
# <span data-ttu-id="26125-101">Get-AzCdnProfileSsoUrl</span><span class="sxs-lookup"><span data-stu-id="26125-101">Get-AzCdnProfileSsoUrl</span></span>

## <span data-ttu-id="26125-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="26125-102">SYNOPSIS</span></span>
<span data-ttu-id="26125-103">Obtém a URL de logon único de um perfil CDN.</span><span class="sxs-lookup"><span data-stu-id="26125-103">Gets the single sign-on URL of a CDN profile.</span></span>

## <span data-ttu-id="26125-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="26125-104">SYNTAX</span></span>

### <span data-ttu-id="26125-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="26125-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnProfileSsoUrl -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="26125-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="26125-106">ByObjectParameterSet</span></span>
```
Get-AzCdnProfileSsoUrl -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="26125-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="26125-107">DESCRIPTION</span></span>
<span data-ttu-id="26125-108">O cmdlet **Get-AzCdnProfileSsoUrl** Obtém a URL de logon único do perfil da CDN (rede de distribuição de conteúdo) do Azure.</span><span class="sxs-lookup"><span data-stu-id="26125-108">The **Get-AzCdnProfileSsoUrl** cmdlet gets the single sign-on URL of the Azure Content Delivery Network (CDN) profile.</span></span>
<span data-ttu-id="26125-109">Esta URL permite que os usuários se conectem a um portal complementar e usem recursos adicionais da CDN.</span><span class="sxs-lookup"><span data-stu-id="26125-109">This URL lets users connect to a supplementary portal and use additional features of  CDN.</span></span>

## <span data-ttu-id="26125-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="26125-110">EXAMPLES</span></span>

## <span data-ttu-id="26125-111">OS</span><span class="sxs-lookup"><span data-stu-id="26125-111">PARAMETERS</span></span>

### <span data-ttu-id="26125-112">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="26125-112">-CdnProfile</span></span>
<span data-ttu-id="26125-113">Especifica o perfil CDN.</span><span class="sxs-lookup"><span data-stu-id="26125-113">Specifies the CDN profile.</span></span>

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

### <span data-ttu-id="26125-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26125-114">-DefaultProfile</span></span>
<span data-ttu-id="26125-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="26125-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="26125-116">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="26125-116">-ProfileName</span></span>
<span data-ttu-id="26125-117">Especifica o nome do perfil CDN.</span><span class="sxs-lookup"><span data-stu-id="26125-117">Specifies the name of the CDN profile.</span></span>

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

### <span data-ttu-id="26125-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26125-118">-ResourceGroupName</span></span>
<span data-ttu-id="26125-119">Especifica o nome do nome do grupo de recursos ao qual o perfil pertence.</span><span class="sxs-lookup"><span data-stu-id="26125-119">Specifies the name of the resource group name to which the profile belongs.</span></span>

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

### <span data-ttu-id="26125-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26125-120">CommonParameters</span></span>
<span data-ttu-id="26125-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26125-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26125-122">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="26125-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26125-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="26125-123">INPUTS</span></span>

### <span data-ttu-id="26125-124">Microsoft. Azure. Commands. cdn. Models. Profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="26125-124">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="26125-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="26125-125">OUTPUTS</span></span>

### <span data-ttu-id="26125-126">Microsoft. Azure. Commands. cdn. Models. Profile. PSSsoUri</span><span class="sxs-lookup"><span data-stu-id="26125-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSSsoUri</span></span>

## <span data-ttu-id="26125-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="26125-127">NOTES</span></span>

## <span data-ttu-id="26125-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="26125-128">RELATED LINKS</span></span>

[<span data-ttu-id="26125-129">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="26125-129">Get-AzCdnProfile</span></span>](./Get-AzCdnProfile.md)


