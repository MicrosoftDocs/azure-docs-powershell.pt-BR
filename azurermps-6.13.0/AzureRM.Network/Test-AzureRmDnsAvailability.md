---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 556A9F12-DF72-468F-9C3F-A747CC70BD2F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/test-azurermdnsavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmDnsAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmDnsAvailability.md
ms.openlocfilehash: 348fd7e97566520b27163de91d4d52162d4c3978
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431334"
---
# <span data-ttu-id="52232-101">Test-AzureRmDnsAvailability</span><span class="sxs-lookup"><span data-stu-id="52232-101">Test-AzureRmDnsAvailability</span></span>

## <span data-ttu-id="52232-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="52232-102">SYNOPSIS</span></span>
<span data-ttu-id="52232-103">Verifica se um nome de domínio na zona cloudapp.azure.com está disponível para uso.</span><span class="sxs-lookup"><span data-stu-id="52232-103">Checks whether a domain name in the cloudapp.azure.com zone is available for use.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="52232-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="52232-104">SYNTAX</span></span>

```
Test-AzureRmDnsAvailability -DomainNameLabel <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="52232-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="52232-105">DESCRIPTION</span></span>
<span data-ttu-id="52232-106">Verifica se um nome de domínio na zona cloudapp.azure.com está disponível para uso.</span><span class="sxs-lookup"><span data-stu-id="52232-106">Checks whether a domain name in the cloudapp.azure.com zone is available for use.</span></span>

## <span data-ttu-id="52232-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="52232-107">EXAMPLES</span></span>

### <span data-ttu-id="52232-108">Exemplo 1: verificar se o contoso.cloudapp.azure.com está disponível para uso.</span><span class="sxs-lookup"><span data-stu-id="52232-108">Example 1: Check if contoso.cloudapp.azure.com is available for use.</span></span>
```
Test-AzureRmDnsAvailability -DomainNameLabel contoso -Location westus
```

## <span data-ttu-id="52232-109">OS</span><span class="sxs-lookup"><span data-stu-id="52232-109">PARAMETERS</span></span>

### <span data-ttu-id="52232-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52232-110">-DefaultProfile</span></span>
<span data-ttu-id="52232-111">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="52232-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52232-112">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="52232-112">-DomainNameLabel</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DomainQualifiedName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52232-113">-Local</span><span class="sxs-lookup"><span data-stu-id="52232-113">-Location</span></span>
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

### <span data-ttu-id="52232-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52232-114">CommonParameters</span></span>
<span data-ttu-id="52232-115">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52232-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52232-116">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52232-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52232-117">SENSORES</span><span class="sxs-lookup"><span data-stu-id="52232-117">INPUTS</span></span>

### <span data-ttu-id="52232-118">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="52232-118">None</span></span>

## <span data-ttu-id="52232-119">EXIBE</span><span class="sxs-lookup"><span data-stu-id="52232-119">OUTPUTS</span></span>

### <span data-ttu-id="52232-120">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="52232-120">System.Boolean</span></span>

## <span data-ttu-id="52232-121">INFORMA</span><span class="sxs-lookup"><span data-stu-id="52232-121">NOTES</span></span>

## <span data-ttu-id="52232-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="52232-122">RELATED LINKS</span></span>
