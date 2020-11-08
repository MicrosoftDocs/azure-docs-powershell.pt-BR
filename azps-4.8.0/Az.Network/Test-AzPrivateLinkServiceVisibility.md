---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-azprivatelinkservicevisibility
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzPrivateLinkServiceVisibility.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzPrivateLinkServiceVisibility.md
ms.openlocfilehash: f443928a8a616e8b8c6c13e5ae941aff607638ef
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94111501"
---
# <span data-ttu-id="8e85f-101">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="8e85f-101">Test-AzPrivateLinkServiceVisibility</span></span>

## <span data-ttu-id="8e85f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8e85f-102">SYNOPSIS</span></span>
<span data-ttu-id="8e85f-103">O **AzPrivateLinkServiceVisibility de teste** verifica se um serviço de link privado está visível para uso atual.</span><span class="sxs-lookup"><span data-stu-id="8e85f-103">The **Test-AzPrivateLinkServiceVisibility** checks whether a private link service is visible for current use.</span></span>

## <span data-ttu-id="8e85f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8e85f-104">SYNTAX</span></span>

```
Test-AzPrivateLinkServiceVisibility -Location <String> [-ResourceGroupName <String>]
 -PrivateLinkServiceAlias <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8e85f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8e85f-105">DESCRIPTION</span></span>
<span data-ttu-id="8e85f-106">Verifique se um serviço de link privado está visível para uso atual.</span><span class="sxs-lookup"><span data-stu-id="8e85f-106">Check whether a private link service is visible for current use.</span></span>

## <span data-ttu-id="8e85f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8e85f-107">EXAMPLES</span></span>

### <span data-ttu-id="8e85f-108">Exemplo 1: verificar se o contoso.cloudapp.azure.com está disponível para uso.</span><span class="sxs-lookup"><span data-stu-id="8e85f-108">Example 1: Check if contoso.cloudapp.azure.com is available for use.</span></span>
```
Test-AzPrivateLinkServiceVisibility -Location westus -PrivateLinkServiceAlias "TestPLS.00000000-0000-0000-0000-000000000000.azure.privatelinkservice"
```

## <span data-ttu-id="8e85f-109">OS</span><span class="sxs-lookup"><span data-stu-id="8e85f-109">PARAMETERS</span></span>

### <span data-ttu-id="8e85f-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e85f-110">-DefaultProfile</span></span>
<span data-ttu-id="8e85f-111">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8e85f-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e85f-112">-Local</span><span class="sxs-lookup"><span data-stu-id="8e85f-112">-Location</span></span>
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

### <span data-ttu-id="8e85f-113">-PrivateLinkServiceAlias</span><span class="sxs-lookup"><span data-stu-id="8e85f-113">-PrivateLinkServiceAlias</span></span>
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

### <span data-ttu-id="8e85f-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e85f-114">-ResourceGroupName</span></span>
<span data-ttu-id="8e85f-115">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8e85f-115">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="8e85f-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e85f-116">CommonParameters</span></span>
<span data-ttu-id="8e85f-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e85f-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e85f-118">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8e85f-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e85f-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8e85f-119">INPUTS</span></span>

### <span data-ttu-id="8e85f-120">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="8e85f-120">None</span></span>

## <span data-ttu-id="8e85f-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8e85f-121">OUTPUTS</span></span>

### <span data-ttu-id="8e85f-122">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8e85f-122">System.Boolean</span></span>

## <span data-ttu-id="8e85f-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8e85f-123">NOTES</span></span>

## <span data-ttu-id="8e85f-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8e85f-124">RELATED LINKS</span></span>
