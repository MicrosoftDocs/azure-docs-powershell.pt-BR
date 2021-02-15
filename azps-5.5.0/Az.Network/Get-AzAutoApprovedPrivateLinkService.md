---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azautoapprovedprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAutoApprovedPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAutoApprovedPrivateLinkService.md
ms.openlocfilehash: b03aad1f76c5151746d50e69bc48ccf10e60842f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114171"
---
# <span data-ttu-id="001dd-101">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="001dd-101">Get-AzAutoApprovedPrivateLinkService</span></span>

## <span data-ttu-id="001dd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="001dd-102">SYNOPSIS</span></span>
<span data-ttu-id="001dd-103">Obtém uma matriz de ID de serviço de link particular que pode ser vinculada a um ponto de extremidade particular com aprovação automática.</span><span class="sxs-lookup"><span data-stu-id="001dd-103">Gets an array of private link service id that can be linked to a private end point with auto approved.</span></span>

## <span data-ttu-id="001dd-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="001dd-104">SYNTAX</span></span>

```
Get-AzAutoApprovedPrivateLinkService -Location <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="001dd-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="001dd-105">DESCRIPTION</span></span>
<span data-ttu-id="001dd-106">O **Get-AzAutoApprovedPrivateLinkService** obtém uma matriz de ID de serviço de link privado que pode ser vinculada a um ponto de extremidade particular com aprovação automática.</span><span class="sxs-lookup"><span data-stu-id="001dd-106">The **Get-AzAutoApprovedPrivateLinkService** gets an array of private link service id that can be linked to a private end point with auto approved.</span></span>

## <span data-ttu-id="001dd-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="001dd-107">EXAMPLES</span></span>

### <span data-ttu-id="001dd-108">Exemplo</span><span class="sxs-lookup"><span data-stu-id="001dd-108">Example</span></span>
```
Get-AzAutoApprovedPrivateLinkService -Location westus -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="001dd-109">Este exemplo retorna uma matriz de ID de serviço de vínculo privado que pode ser vinculada a um ponto de extremidade particular com aprovação automática.</span><span class="sxs-lookup"><span data-stu-id="001dd-109">This example return an array of private link service id that can be linked to a private end point with auto approved.</span></span>

## <span data-ttu-id="001dd-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="001dd-110">PARAMETERS</span></span>

### <span data-ttu-id="001dd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="001dd-111">-DefaultProfile</span></span>
<span data-ttu-id="001dd-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="001dd-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="001dd-113">-Local</span><span class="sxs-lookup"><span data-stu-id="001dd-113">-Location</span></span>
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

### <span data-ttu-id="001dd-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="001dd-114">-ResourceGroupName</span></span>
<span data-ttu-id="001dd-115">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="001dd-115">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="001dd-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="001dd-116">CommonParameters</span></span>
<span data-ttu-id="001dd-117">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="001dd-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="001dd-118">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="001dd-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="001dd-119">Entradas</span><span class="sxs-lookup"><span data-stu-id="001dd-119">INPUTS</span></span>

### <span data-ttu-id="001dd-120">Nenhum</span><span class="sxs-lookup"><span data-stu-id="001dd-120">None</span></span>

## <span data-ttu-id="001dd-121">Saídas</span><span class="sxs-lookup"><span data-stu-id="001dd-121">OUTPUTS</span></span>

### <span data-ttu-id="001dd-122">Microsoft.Azure.Commands.Network.Models.PSAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="001dd-122">Microsoft.Azure.Commands.Network.Models.PSAutoApprovedPrivateLinkService</span></span>

## <span data-ttu-id="001dd-123">Notas</span><span class="sxs-lookup"><span data-stu-id="001dd-123">NOTES</span></span>

## <span data-ttu-id="001dd-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="001dd-124">RELATED LINKS</span></span>
