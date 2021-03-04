---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azautoapprovedprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAutoApprovedPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAutoApprovedPrivateLinkService.md
ms.openlocfilehash: 42e7b805e772e42ed395f8893b1140faaab715ba
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890796"
---
# <span data-ttu-id="bbedd-101">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="bbedd-101">Get-AzAutoApprovedPrivateLinkService</span></span>

## <span data-ttu-id="bbedd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bbedd-102">SYNOPSIS</span></span>
<span data-ttu-id="bbedd-103">Obtém uma matriz de ID de serviço de link privado que pode ser vinculada a um ponto de extremidade privado com aprovação automática.</span><span class="sxs-lookup"><span data-stu-id="bbedd-103">Gets an array of private link service id that can be linked to a private end point with auto approved.</span></span>

## <span data-ttu-id="bbedd-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="bbedd-104">SYNTAX</span></span>

```
Get-AzAutoApprovedPrivateLinkService -Location <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bbedd-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="bbedd-105">DESCRIPTION</span></span>
<span data-ttu-id="bbedd-106">O **Get-AzAutoApprovedPrivateLinkService** obtém uma matriz de id de serviço de link privado que pode ser vinculada a um ponto de extremidade privado com aprovação automática.</span><span class="sxs-lookup"><span data-stu-id="bbedd-106">The **Get-AzAutoApprovedPrivateLinkService** gets an array of private link service id that can be linked to a private end point with auto approved.</span></span>

## <span data-ttu-id="bbedd-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bbedd-107">EXAMPLES</span></span>

### <span data-ttu-id="bbedd-108">Exemplo</span><span class="sxs-lookup"><span data-stu-id="bbedd-108">Example</span></span>
```
Get-AzAutoApprovedPrivateLinkService -Location westus -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="bbedd-109">Este exemplo retorna uma matriz de ID de serviço de link privado que pode ser vinculada a um ponto de extremidade privado com aprovação automática.</span><span class="sxs-lookup"><span data-stu-id="bbedd-109">This example return an array of private link service id that can be linked to a private end point with auto approved.</span></span>

## <span data-ttu-id="bbedd-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="bbedd-110">PARAMETERS</span></span>

### <span data-ttu-id="bbedd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbedd-111">-DefaultProfile</span></span>
<span data-ttu-id="bbedd-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bbedd-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bbedd-113">-Location</span><span class="sxs-lookup"><span data-stu-id="bbedd-113">-Location</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbedd-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bbedd-114">-ResourceGroupName</span></span>
<span data-ttu-id="bbedd-115">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="bbedd-115">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="bbedd-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbedd-116">CommonParameters</span></span>
<span data-ttu-id="bbedd-117">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bbedd-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbedd-118">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bbedd-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbedd-119">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bbedd-119">INPUTS</span></span>

### <span data-ttu-id="bbedd-120">Nenhum</span><span class="sxs-lookup"><span data-stu-id="bbedd-120">None</span></span>

## <span data-ttu-id="bbedd-121">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="bbedd-121">OUTPUTS</span></span>

### <span data-ttu-id="bbedd-122">Microsoft.Azure.Commands.Network.Models.PSAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="bbedd-122">Microsoft.Azure.Commands.Network.Models.PSAutoApprovedPrivateLinkService</span></span>

## <span data-ttu-id="bbedd-123">NOTES</span><span class="sxs-lookup"><span data-stu-id="bbedd-123">NOTES</span></span>

## <span data-ttu-id="bbedd-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bbedd-124">RELATED LINKS</span></span>
