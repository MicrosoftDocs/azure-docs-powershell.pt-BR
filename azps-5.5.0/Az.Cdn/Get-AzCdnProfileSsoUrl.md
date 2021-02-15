---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 93D5E2D9-FB89-4311-8E8E-44CBFAFC98A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnprofilessourl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSsoUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSsoUrl.md
ms.openlocfilehash: 74bc4fae4dd55a85c4aca811819a0348f5df5f2c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112179"
---
# <span data-ttu-id="9bd63-101">Get-AzCdnProfileSsoUrl</span><span class="sxs-lookup"><span data-stu-id="9bd63-101">Get-AzCdnProfileSsoUrl</span></span>

## <span data-ttu-id="9bd63-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9bd63-102">SYNOPSIS</span></span>
<span data-ttu-id="9bd63-103">Obtém a URL de entrada única de um perfil de CDN.</span><span class="sxs-lookup"><span data-stu-id="9bd63-103">Gets the single sign-on URL of a CDN profile.</span></span>

## <span data-ttu-id="9bd63-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9bd63-104">SYNTAX</span></span>

### <span data-ttu-id="9bd63-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="9bd63-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnProfileSsoUrl -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9bd63-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9bd63-106">ByObjectParameterSet</span></span>
```
Get-AzCdnProfileSsoUrl -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9bd63-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="9bd63-107">DESCRIPTION</span></span>
<span data-ttu-id="9bd63-108">O cmdlet **Get-AzCdnProfileSsoUrl** obtém a URL de entrada única do perfil de REDE de Distribuição de Conteúdo (CDN) do Azure.</span><span class="sxs-lookup"><span data-stu-id="9bd63-108">The **Get-AzCdnProfileSsoUrl** cmdlet gets the single sign-on URL of the Azure Content Delivery Network (CDN) profile.</span></span>
<span data-ttu-id="9bd63-109">Essa URL permite que os usuários se conectem a um portal complementar e usem recursos adicionais de CDN.</span><span class="sxs-lookup"><span data-stu-id="9bd63-109">This URL lets users connect to a supplementary portal and use additional features of  CDN.</span></span>

## <span data-ttu-id="9bd63-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9bd63-110">EXAMPLES</span></span>

## <span data-ttu-id="9bd63-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9bd63-111">PARAMETERS</span></span>

### <span data-ttu-id="9bd63-112">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="9bd63-112">-CdnProfile</span></span>
<span data-ttu-id="9bd63-113">Especifica o perfil da CDN.</span><span class="sxs-lookup"><span data-stu-id="9bd63-113">Specifies the CDN profile.</span></span>

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

### <span data-ttu-id="9bd63-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bd63-114">-DefaultProfile</span></span>
<span data-ttu-id="9bd63-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="9bd63-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9bd63-116">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="9bd63-116">-ProfileName</span></span>
<span data-ttu-id="9bd63-117">Especifica o nome do perfil da CDN.</span><span class="sxs-lookup"><span data-stu-id="9bd63-117">Specifies the name of the CDN profile.</span></span>

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

### <span data-ttu-id="9bd63-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9bd63-118">-ResourceGroupName</span></span>
<span data-ttu-id="9bd63-119">Especifica o nome do grupo de recursos ao qual o perfil pertence.</span><span class="sxs-lookup"><span data-stu-id="9bd63-119">Specifies the name of the resource group name to which the profile belongs.</span></span>

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

### <span data-ttu-id="9bd63-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bd63-120">CommonParameters</span></span>
<span data-ttu-id="9bd63-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9bd63-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bd63-122">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9bd63-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bd63-123">Entradas</span><span class="sxs-lookup"><span data-stu-id="9bd63-123">INPUTS</span></span>

### <span data-ttu-id="9bd63-124">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="9bd63-124">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="9bd63-125">Saídas</span><span class="sxs-lookup"><span data-stu-id="9bd63-125">OUTPUTS</span></span>

### <span data-ttu-id="9bd63-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSSsoUri</span><span class="sxs-lookup"><span data-stu-id="9bd63-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSSsoUri</span></span>

## <span data-ttu-id="9bd63-127">Notas</span><span class="sxs-lookup"><span data-stu-id="9bd63-127">NOTES</span></span>

## <span data-ttu-id="9bd63-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9bd63-128">RELATED LINKS</span></span>

[<span data-ttu-id="9bd63-129">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="9bd63-129">Get-AzCdnProfile</span></span>](./Get-AzCdnProfile.md)


