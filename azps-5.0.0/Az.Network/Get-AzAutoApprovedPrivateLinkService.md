---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azautoapprovedprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAutoApprovedPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAutoApprovedPrivateLinkService.md
ms.openlocfilehash: b03aad1f76c5151746d50e69bc48ccf10e60842f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94125909"
---
# <span data-ttu-id="7d4a0-101">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="7d4a0-101">Get-AzAutoApprovedPrivateLinkService</span></span>

## <span data-ttu-id="7d4a0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7d4a0-102">SYNOPSIS</span></span>
<span data-ttu-id="7d4a0-103">Obtém uma matriz de ID de serviço de link privado que pode ser vinculada a um ponto de extremidade privado com aprovação automática.</span><span class="sxs-lookup"><span data-stu-id="7d4a0-103">Gets an array of private link service id that can be linked to a private end point with auto approved.</span></span>

## <span data-ttu-id="7d4a0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7d4a0-104">SYNTAX</span></span>

```
Get-AzAutoApprovedPrivateLinkService -Location <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7d4a0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7d4a0-105">DESCRIPTION</span></span>
<span data-ttu-id="7d4a0-106">**Get-AzAutoApprovedPrivateLinkService** Obtém uma matriz de ID de serviço de link privado que pode ser vinculada a um ponto de extremidade privado com aprovação automática.</span><span class="sxs-lookup"><span data-stu-id="7d4a0-106">The **Get-AzAutoApprovedPrivateLinkService** gets an array of private link service id that can be linked to a private end point with auto approved.</span></span>

## <span data-ttu-id="7d4a0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7d4a0-107">EXAMPLES</span></span>

### <span data-ttu-id="7d4a0-108">Exemplo</span><span class="sxs-lookup"><span data-stu-id="7d4a0-108">Example</span></span>
```
Get-AzAutoApprovedPrivateLinkService -Location westus -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="7d4a0-109">Este exemplo retorna uma matriz de ID de serviço de link privado que pode ser vinculada a um ponto de extremidade privado com aprovação automática.</span><span class="sxs-lookup"><span data-stu-id="7d4a0-109">This example return an array of private link service id that can be linked to a private end point with auto approved.</span></span>

## <span data-ttu-id="7d4a0-110">OS</span><span class="sxs-lookup"><span data-stu-id="7d4a0-110">PARAMETERS</span></span>

### <span data-ttu-id="7d4a0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d4a0-111">-DefaultProfile</span></span>
<span data-ttu-id="7d4a0-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7d4a0-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d4a0-113">-Local</span><span class="sxs-lookup"><span data-stu-id="7d4a0-113">-Location</span></span>
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

### <span data-ttu-id="7d4a0-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d4a0-114">-ResourceGroupName</span></span>
<span data-ttu-id="7d4a0-115">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7d4a0-115">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="7d4a0-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d4a0-116">CommonParameters</span></span>
<span data-ttu-id="7d4a0-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d4a0-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d4a0-118">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7d4a0-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d4a0-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7d4a0-119">INPUTS</span></span>

### <span data-ttu-id="7d4a0-120">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="7d4a0-120">None</span></span>

## <span data-ttu-id="7d4a0-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7d4a0-121">OUTPUTS</span></span>

### <span data-ttu-id="7d4a0-122">Microsoft. Azure. Commands. Network. Models. PSAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="7d4a0-122">Microsoft.Azure.Commands.Network.Models.PSAutoApprovedPrivateLinkService</span></span>

## <span data-ttu-id="7d4a0-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7d4a0-123">NOTES</span></span>

## <span data-ttu-id="7d4a0-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7d4a0-124">RELATED LINKS</span></span>
