---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: C0BEC701-8CE2-4B19-9F04-D32A42D9249E
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/get-azrediscachekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheKey.md
ms.openlocfilehash: 96eed93e4020384b0c989a05f549aa21f5482493
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773420"
---
# <span data-ttu-id="a0df0-101">Get-AzRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="a0df0-101">Get-AzRedisCacheKey</span></span>

## <span data-ttu-id="a0df0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a0df0-102">SYNOPSIS</span></span>
<span data-ttu-id="a0df0-103">Obtém as teclas de acesso para um cache Redis.</span><span class="sxs-lookup"><span data-stu-id="a0df0-103">Gets the access keys for a Redis Cache.</span></span>

## <span data-ttu-id="a0df0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a0df0-104">SYNTAX</span></span>

```
Get-AzRedisCacheKey [-ResourceGroupName <String>] -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a0df0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a0df0-105">DESCRIPTION</span></span>
<span data-ttu-id="a0df0-106">O cmdlet **Get-AzRedisCacheKey** Obtém as teclas de acesso para um cache do Redis do Azure.</span><span class="sxs-lookup"><span data-stu-id="a0df0-106">The **Get-AzRedisCacheKey** cmdlet gets the access keys for an Azure Redis Cache.</span></span>

## <span data-ttu-id="a0df0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a0df0-107">EXAMPLES</span></span>

### <span data-ttu-id="a0df0-108">Exemplo 1: obter as teclas de acesso para um cache Redis</span><span class="sxs-lookup"><span data-stu-id="a0df0-108">Example 1: Get the access keys for a Redis Cache</span></span>
```
PS C:\>Get-AzRedisCacheKey -ResourceGroupName "MyResourceGroup" -Name "MyCacheKey"
PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="a0df0-109">Esse comando obtém as teclas de acesso chamadas MyCacheKey.</span><span class="sxs-lookup"><span data-stu-id="a0df0-109">This command gets the access keys named MyCacheKey.</span></span>

## <span data-ttu-id="a0df0-110">OS</span><span class="sxs-lookup"><span data-stu-id="a0df0-110">PARAMETERS</span></span>

### <span data-ttu-id="a0df0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0df0-111">-DefaultProfile</span></span>
<span data-ttu-id="a0df0-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a0df0-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a0df0-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="a0df0-113">-Name</span></span>
<span data-ttu-id="a0df0-114">Especifica o nome de um cache Redis.</span><span class="sxs-lookup"><span data-stu-id="a0df0-114">Specifies the name of a Redis Cache.</span></span>

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

### <span data-ttu-id="a0df0-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0df0-115">-ResourceGroupName</span></span>
<span data-ttu-id="a0df0-116">Especifica o nome do grupo de recursos que contém o cache Redis.</span><span class="sxs-lookup"><span data-stu-id="a0df0-116">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="a0df0-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0df0-117">CommonParameters</span></span>
<span data-ttu-id="a0df0-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0df0-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0df0-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0df0-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0df0-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a0df0-120">INPUTS</span></span>

### <span data-ttu-id="a0df0-121">System. String</span><span class="sxs-lookup"><span data-stu-id="a0df0-121">System.String</span></span>

## <span data-ttu-id="a0df0-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a0df0-122">OUTPUTS</span></span>

### <span data-ttu-id="a0df0-123">Microsoft. Azure. Management. Redis. Models. RedisAccessKeys</span><span class="sxs-lookup"><span data-stu-id="a0df0-123">Microsoft.Azure.Management.Redis.Models.RedisAccessKeys</span></span>

## <span data-ttu-id="a0df0-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a0df0-124">NOTES</span></span>

## <span data-ttu-id="a0df0-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a0df0-125">RELATED LINKS</span></span>

[<span data-ttu-id="a0df0-126">New-AzRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="a0df0-126">New-AzRedisCacheKey</span></span>](./New-AzRedisCacheKey.md)


