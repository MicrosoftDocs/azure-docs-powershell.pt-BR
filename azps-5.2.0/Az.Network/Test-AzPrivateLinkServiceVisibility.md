---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-azprivatelinkservicevisibility
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzPrivateLinkServiceVisibility.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzPrivateLinkServiceVisibility.md
ms.openlocfilehash: f443928a8a616e8b8c6c13e5ae941aff607638ef
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98256737"
---
# <span data-ttu-id="4b2df-101">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="4b2df-101">Test-AzPrivateLinkServiceVisibility</span></span>

## <span data-ttu-id="4b2df-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4b2df-102">SYNOPSIS</span></span>
<span data-ttu-id="4b2df-103">O **AzPrivateLinkServiceVisibility de teste** verifica se um serviço de link privado está visível para uso atual.</span><span class="sxs-lookup"><span data-stu-id="4b2df-103">The **Test-AzPrivateLinkServiceVisibility** checks whether a private link service is visible for current use.</span></span>

## <span data-ttu-id="4b2df-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4b2df-104">SYNTAX</span></span>

```
Test-AzPrivateLinkServiceVisibility -Location <String> [-ResourceGroupName <String>]
 -PrivateLinkServiceAlias <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4b2df-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4b2df-105">DESCRIPTION</span></span>
<span data-ttu-id="4b2df-106">Verifique se um serviço de link privado está visível para uso atual.</span><span class="sxs-lookup"><span data-stu-id="4b2df-106">Check whether a private link service is visible for current use.</span></span>

## <span data-ttu-id="4b2df-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4b2df-107">EXAMPLES</span></span>

### <span data-ttu-id="4b2df-108">Exemplo 1: verificar se o contoso.cloudapp.azure.com está disponível para uso.</span><span class="sxs-lookup"><span data-stu-id="4b2df-108">Example 1: Check if contoso.cloudapp.azure.com is available for use.</span></span>
```
Test-AzPrivateLinkServiceVisibility -Location westus -PrivateLinkServiceAlias "TestPLS.00000000-0000-0000-0000-000000000000.azure.privatelinkservice"
```

## <span data-ttu-id="4b2df-109">OS</span><span class="sxs-lookup"><span data-stu-id="4b2df-109">PARAMETERS</span></span>

### <span data-ttu-id="4b2df-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b2df-110">-DefaultProfile</span></span>
<span data-ttu-id="4b2df-111">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4b2df-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b2df-112">-Local</span><span class="sxs-lookup"><span data-stu-id="4b2df-112">-Location</span></span>
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

### <span data-ttu-id="4b2df-113">-PrivateLinkServiceAlias</span><span class="sxs-lookup"><span data-stu-id="4b2df-113">-PrivateLinkServiceAlias</span></span>
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

### <span data-ttu-id="4b2df-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b2df-114">-ResourceGroupName</span></span>
<span data-ttu-id="4b2df-115">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4b2df-115">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="4b2df-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b2df-116">CommonParameters</span></span>
<span data-ttu-id="4b2df-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b2df-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b2df-118">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4b2df-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b2df-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4b2df-119">INPUTS</span></span>

### <span data-ttu-id="4b2df-120">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="4b2df-120">None</span></span>

## <span data-ttu-id="4b2df-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4b2df-121">OUTPUTS</span></span>

### <span data-ttu-id="4b2df-122">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4b2df-122">System.Boolean</span></span>

## <span data-ttu-id="4b2df-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4b2df-123">NOTES</span></span>

## <span data-ttu-id="4b2df-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4b2df-124">RELATED LINKS</span></span>
