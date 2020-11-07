---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-azprivatelinkservicevisibility
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzPrivateLinkServiceVisibility.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzPrivateLinkServiceVisibility.md
ms.openlocfilehash: e05ea63bddc8dc61332a31e4fa44aa1b7428055a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772690"
---
# <span data-ttu-id="d450c-101">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="d450c-101">Test-AzPrivateLinkServiceVisibility</span></span>

## <span data-ttu-id="d450c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d450c-102">SYNOPSIS</span></span>
<span data-ttu-id="d450c-103">O **AzPrivateLinkServiceVisibility de teste** verifica se um serviço de link privado está visível para uso atual.</span><span class="sxs-lookup"><span data-stu-id="d450c-103">The **Test-AzPrivateLinkServiceVisibility** checks whether a private link service is visible for current use.</span></span>

## <span data-ttu-id="d450c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d450c-104">SYNTAX</span></span>

```
Test-AzPrivateLinkServiceVisibility -Location <String> [-ResourceGroupName <String>]
 -PrivateLinkServiceAlias <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d450c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d450c-105">DESCRIPTION</span></span>
<span data-ttu-id="d450c-106">Verifique se um serviço de link privado está visível para uso atual.</span><span class="sxs-lookup"><span data-stu-id="d450c-106">Check whether a private link service is visible for current use.</span></span>

## <span data-ttu-id="d450c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d450c-107">EXAMPLES</span></span>

### <span data-ttu-id="d450c-108">Exemplo 1: verificar se o contoso.cloudapp.azure.com está disponível para uso.</span><span class="sxs-lookup"><span data-stu-id="d450c-108">Example 1: Check if contoso.cloudapp.azure.com is available for use.</span></span>
```
Test-AzPrivateLinkServiceVisibility -Location westus -PrivateLinkServiceAlias "TestPLS.00000000-0000-0000-0000-000000000000.azure.privatelinkservice"
```

## <span data-ttu-id="d450c-109">OS</span><span class="sxs-lookup"><span data-stu-id="d450c-109">PARAMETERS</span></span>

### <span data-ttu-id="d450c-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d450c-110">-DefaultProfile</span></span>
<span data-ttu-id="d450c-111">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d450c-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d450c-112">-Local</span><span class="sxs-lookup"><span data-stu-id="d450c-112">-Location</span></span>
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

### <span data-ttu-id="d450c-113">-PrivateLinkServiceAlias</span><span class="sxs-lookup"><span data-stu-id="d450c-113">-PrivateLinkServiceAlias</span></span>
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

### <span data-ttu-id="d450c-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d450c-114">-ResourceGroupName</span></span>
<span data-ttu-id="d450c-115">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d450c-115">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="d450c-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d450c-116">CommonParameters</span></span>
<span data-ttu-id="d450c-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d450c-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d450c-118">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d450c-118">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d450c-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d450c-119">INPUTS</span></span>

### <span data-ttu-id="d450c-120">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="d450c-120">None</span></span>

## <span data-ttu-id="d450c-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d450c-121">OUTPUTS</span></span>

### <span data-ttu-id="d450c-122">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d450c-122">System.Boolean</span></span>

## <span data-ttu-id="d450c-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d450c-123">NOTES</span></span>

## <span data-ttu-id="d450c-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d450c-124">RELATED LINKS</span></span>
