---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/test-azprivatelinkservicevisibility
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzPrivateLinkServiceVisibility.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzPrivateLinkServiceVisibility.md
ms.openlocfilehash: 3fe05034734a4cfb0d511921372e41b00d7b457c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885350"
---
# <span data-ttu-id="10248-101">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="10248-101">Test-AzPrivateLinkServiceVisibility</span></span>

## <span data-ttu-id="10248-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10248-102">SYNOPSIS</span></span>
<span data-ttu-id="10248-103">O **Test-AzPrivateLinkServiceVisibility** verifica se um serviço de link privado está visível para uso atual.</span><span class="sxs-lookup"><span data-stu-id="10248-103">The **Test-AzPrivateLinkServiceVisibility** checks whether a private link service is visible for current use.</span></span>

## <span data-ttu-id="10248-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="10248-104">SYNTAX</span></span>

```
Test-AzPrivateLinkServiceVisibility -Location <String> [-ResourceGroupName <String>]
 -PrivateLinkServiceAlias <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10248-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="10248-105">DESCRIPTION</span></span>
<span data-ttu-id="10248-106">Verifique se um serviço de link privado está visível para uso atual.</span><span class="sxs-lookup"><span data-stu-id="10248-106">Check whether a private link service is visible for current use.</span></span>

## <span data-ttu-id="10248-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="10248-107">EXAMPLES</span></span>

### <span data-ttu-id="10248-108">Exemplo 1: verifique se contoso.cloudapp.azure.com está disponível para uso.</span><span class="sxs-lookup"><span data-stu-id="10248-108">Example 1: Check if contoso.cloudapp.azure.com is available for use.</span></span>
```
Test-AzPrivateLinkServiceVisibility -Location westus -PrivateLinkServiceAlias "TestPLS.00000000-0000-0000-0000-000000000000.azure.privatelinkservice"
```

## <span data-ttu-id="10248-109">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="10248-109">PARAMETERS</span></span>

### <span data-ttu-id="10248-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10248-110">-DefaultProfile</span></span>
<span data-ttu-id="10248-111">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="10248-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10248-112">-Location</span><span class="sxs-lookup"><span data-stu-id="10248-112">-Location</span></span>
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

### <span data-ttu-id="10248-113">-PrivateLinkServiceAlias</span><span class="sxs-lookup"><span data-stu-id="10248-113">-PrivateLinkServiceAlias</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10248-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10248-114">-ResourceGroupName</span></span>
<span data-ttu-id="10248-115">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="10248-115">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="10248-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10248-116">CommonParameters</span></span>
<span data-ttu-id="10248-117">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10248-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10248-118">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="10248-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10248-119">INPUTS</span><span class="sxs-lookup"><span data-stu-id="10248-119">INPUTS</span></span>

### <span data-ttu-id="10248-120">Nenhum</span><span class="sxs-lookup"><span data-stu-id="10248-120">None</span></span>

## <span data-ttu-id="10248-121">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="10248-121">OUTPUTS</span></span>

### <span data-ttu-id="10248-122">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="10248-122">System.Boolean</span></span>

## <span data-ttu-id="10248-123">NOTES</span><span class="sxs-lookup"><span data-stu-id="10248-123">NOTES</span></span>

## <span data-ttu-id="10248-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="10248-124">RELATED LINKS</span></span>
