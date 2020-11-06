---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: C0BEC701-8CE2-4B19-9F04-D32A42D9249E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/get-azurermrediscachekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCacheKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCacheKey.md
ms.openlocfilehash: 297d02fcb77c8fc537831b2b1995bfe43ca90e73
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430071"
---
# <span data-ttu-id="896df-101">Get-AzureRmRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="896df-101">Get-AzureRmRedisCacheKey</span></span>

## <span data-ttu-id="896df-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="896df-102">SYNOPSIS</span></span>
<span data-ttu-id="896df-103">Obtém as teclas de acesso para um cache Redis.</span><span class="sxs-lookup"><span data-stu-id="896df-103">Gets the access keys for a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="896df-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="896df-104">SYNTAX</span></span>

```
Get-AzureRmRedisCacheKey [-ResourceGroupName <String>] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="896df-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="896df-105">DESCRIPTION</span></span>
<span data-ttu-id="896df-106">O cmdlet **Get-AzureRmRedisCacheKey** Obtém as teclas de acesso para um cache do Redis do Azure.</span><span class="sxs-lookup"><span data-stu-id="896df-106">The **Get-AzureRmRedisCacheKey** cmdlet gets the access keys for an Azure Redis Cache.</span></span>

## <span data-ttu-id="896df-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="896df-107">EXAMPLES</span></span>

### <span data-ttu-id="896df-108">Exemplo 1: obter as teclas de acesso para um cache Redis</span><span class="sxs-lookup"><span data-stu-id="896df-108">Example 1: Get the access keys for a Redis Cache</span></span>
```
PS C:\>Get-AzureRmRedisCacheKey -ResourceGroupName "MyResourceGroup" -Name "MyCacheKey"
PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="896df-109">Esse comando obtém as teclas de acesso chamadas MyCacheKey.</span><span class="sxs-lookup"><span data-stu-id="896df-109">This command gets the access keys named MyCacheKey.</span></span>

## <span data-ttu-id="896df-110">OS</span><span class="sxs-lookup"><span data-stu-id="896df-110">PARAMETERS</span></span>

### <span data-ttu-id="896df-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="896df-111">-DefaultProfile</span></span>
<span data-ttu-id="896df-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="896df-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="896df-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="896df-113">-Name</span></span>
<span data-ttu-id="896df-114">Especifica o nome de um cache Redis.</span><span class="sxs-lookup"><span data-stu-id="896df-114">Specifies the name of a Redis Cache.</span></span>

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

### <span data-ttu-id="896df-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="896df-115">-ResourceGroupName</span></span>
<span data-ttu-id="896df-116">Especifica o nome do grupo de recursos que contém o cache Redis.</span><span class="sxs-lookup"><span data-stu-id="896df-116">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="896df-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="896df-117">CommonParameters</span></span>
<span data-ttu-id="896df-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="896df-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="896df-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="896df-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="896df-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="896df-120">INPUTS</span></span>

### <span data-ttu-id="896df-121">System. String</span><span class="sxs-lookup"><span data-stu-id="896df-121">System.String</span></span>

## <span data-ttu-id="896df-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="896df-122">OUTPUTS</span></span>

### <span data-ttu-id="896df-123">Microsoft. Azure. Management. Redis. Models. RedisAccessKeys</span><span class="sxs-lookup"><span data-stu-id="896df-123">Microsoft.Azure.Management.Redis.Models.RedisAccessKeys</span></span>

## <span data-ttu-id="896df-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="896df-124">NOTES</span></span>

## <span data-ttu-id="896df-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="896df-125">RELATED LINKS</span></span>

[<span data-ttu-id="896df-126">New-AzureRmRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="896df-126">New-AzureRmRedisCacheKey</span></span>](./New-AzureRmRedisCacheKey.md)

