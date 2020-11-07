---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-azprivatelinkservicevisibility
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzPrivateLinkServiceVisibility.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzPrivateLinkServiceVisibility.md
ms.openlocfilehash: f443928a8a616e8b8c6c13e5ae941aff607638ef
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942653"
---
# <span data-ttu-id="e5c8b-101">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="e5c8b-101">Test-AzPrivateLinkServiceVisibility</span></span>

## <span data-ttu-id="e5c8b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e5c8b-102">SYNOPSIS</span></span>
<span data-ttu-id="e5c8b-103">O **AzPrivateLinkServiceVisibility de teste** verifica se um serviço de link privado está visível para uso atual.</span><span class="sxs-lookup"><span data-stu-id="e5c8b-103">The **Test-AzPrivateLinkServiceVisibility** checks whether a private link service is visible for current use.</span></span>

## <span data-ttu-id="e5c8b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e5c8b-104">SYNTAX</span></span>

```
Test-AzPrivateLinkServiceVisibility -Location <String> [-ResourceGroupName <String>]
 -PrivateLinkServiceAlias <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5c8b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e5c8b-105">DESCRIPTION</span></span>
<span data-ttu-id="e5c8b-106">Verifique se um serviço de link privado está visível para uso atual.</span><span class="sxs-lookup"><span data-stu-id="e5c8b-106">Check whether a private link service is visible for current use.</span></span>

## <span data-ttu-id="e5c8b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e5c8b-107">EXAMPLES</span></span>

### <span data-ttu-id="e5c8b-108">Exemplo 1: verificar se o contoso.cloudapp.azure.com está disponível para uso.</span><span class="sxs-lookup"><span data-stu-id="e5c8b-108">Example 1: Check if contoso.cloudapp.azure.com is available for use.</span></span>
```
Test-AzPrivateLinkServiceVisibility -Location westus -PrivateLinkServiceAlias "TestPLS.00000000-0000-0000-0000-000000000000.azure.privatelinkservice"
```

## <span data-ttu-id="e5c8b-109">OS</span><span class="sxs-lookup"><span data-stu-id="e5c8b-109">PARAMETERS</span></span>

### <span data-ttu-id="e5c8b-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5c8b-110">-DefaultProfile</span></span>
<span data-ttu-id="e5c8b-111">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e5c8b-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5c8b-112">-Local</span><span class="sxs-lookup"><span data-stu-id="e5c8b-112">-Location</span></span>
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

### <span data-ttu-id="e5c8b-113">-PrivateLinkServiceAlias</span><span class="sxs-lookup"><span data-stu-id="e5c8b-113">-PrivateLinkServiceAlias</span></span>
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

### <span data-ttu-id="e5c8b-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5c8b-114">-ResourceGroupName</span></span>
<span data-ttu-id="e5c8b-115">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e5c8b-115">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="e5c8b-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5c8b-116">CommonParameters</span></span>
<span data-ttu-id="e5c8b-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5c8b-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5c8b-118">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e5c8b-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5c8b-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e5c8b-119">INPUTS</span></span>

### <span data-ttu-id="e5c8b-120">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="e5c8b-120">None</span></span>

## <span data-ttu-id="e5c8b-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e5c8b-121">OUTPUTS</span></span>

### <span data-ttu-id="e5c8b-122">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e5c8b-122">System.Boolean</span></span>

## <span data-ttu-id="e5c8b-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e5c8b-123">NOTES</span></span>

## <span data-ttu-id="e5c8b-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e5c8b-124">RELATED LINKS</span></span>
