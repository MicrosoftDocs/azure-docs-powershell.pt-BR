---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: C0BEC701-8CE2-4B19-9F04-D32A42D9249E
online version: https://docs.microsoft.com/powershell/module/az.rediscache/get-azrediscachekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheKey.md
ms.openlocfilehash: 1d5f230070f8b8c269137e07b04af970f314d564
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889887"
---
# <span data-ttu-id="d8f6c-101">Get-AzRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="d8f6c-101">Get-AzRedisCacheKey</span></span>

## <span data-ttu-id="d8f6c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8f6c-102">SYNOPSIS</span></span>
<span data-ttu-id="d8f6c-103">Obtém as chaves de acesso para um Cache Redis.</span><span class="sxs-lookup"><span data-stu-id="d8f6c-103">Gets the access keys for a Redis Cache.</span></span>

## <span data-ttu-id="d8f6c-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d8f6c-104">SYNTAX</span></span>

```
Get-AzRedisCacheKey [-ResourceGroupName <String>] -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d8f6c-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d8f6c-105">DESCRIPTION</span></span>
<span data-ttu-id="d8f6c-106">O cmdlet **Get-AzRedisCacheKey** obtém as chaves de acesso para um Cache do Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="d8f6c-106">The **Get-AzRedisCacheKey** cmdlet gets the access keys for an Azure Redis Cache.</span></span>

## <span data-ttu-id="d8f6c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d8f6c-107">EXAMPLES</span></span>

### <span data-ttu-id="d8f6c-108">Exemplo 1: Obter as chaves de acesso para um Cache Redis</span><span class="sxs-lookup"><span data-stu-id="d8f6c-108">Example 1: Get the access keys for a Redis Cache</span></span>
```
PS C:\>Get-AzRedisCacheKey -ResourceGroupName "MyResourceGroup" -Name "MyCacheKey"
PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="d8f6c-109">Este comando obtém as chaves de acesso chamadas MyCacheKey.</span><span class="sxs-lookup"><span data-stu-id="d8f6c-109">This command gets the access keys named MyCacheKey.</span></span>

## <span data-ttu-id="d8f6c-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d8f6c-110">PARAMETERS</span></span>

### <span data-ttu-id="d8f6c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8f6c-111">-DefaultProfile</span></span>
<span data-ttu-id="d8f6c-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="d8f6c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d8f6c-113">-Name</span><span class="sxs-lookup"><span data-stu-id="d8f6c-113">-Name</span></span>
<span data-ttu-id="d8f6c-114">Especifica o nome de um Cache Redis.</span><span class="sxs-lookup"><span data-stu-id="d8f6c-114">Specifies the name of a Redis Cache.</span></span>

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

### <span data-ttu-id="d8f6c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8f6c-115">-ResourceGroupName</span></span>
<span data-ttu-id="d8f6c-116">Especifica o nome do grupo de recursos que contém o Cache Redis.</span><span class="sxs-lookup"><span data-stu-id="d8f6c-116">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="d8f6c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8f6c-117">CommonParameters</span></span>
<span data-ttu-id="d8f6c-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8f6c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8f6c-119">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8f6c-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8f6c-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d8f6c-120">INPUTS</span></span>

### <span data-ttu-id="d8f6c-121">System.String</span><span class="sxs-lookup"><span data-stu-id="d8f6c-121">System.String</span></span>

## <span data-ttu-id="d8f6c-122">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d8f6c-122">OUTPUTS</span></span>

### <span data-ttu-id="d8f6c-123">Microsoft.Azure.Management.Redis.Models.RedisAccessKeys</span><span class="sxs-lookup"><span data-stu-id="d8f6c-123">Microsoft.Azure.Management.Redis.Models.RedisAccessKeys</span></span>

## <span data-ttu-id="d8f6c-124">NOTES</span><span class="sxs-lookup"><span data-stu-id="d8f6c-124">NOTES</span></span>

## <span data-ttu-id="d8f6c-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d8f6c-125">RELATED LINKS</span></span>

[<span data-ttu-id="d8f6c-126">New-AzRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="d8f6c-126">New-AzRedisCacheKey</span></span>](./New-AzRedisCacheKey.md)


