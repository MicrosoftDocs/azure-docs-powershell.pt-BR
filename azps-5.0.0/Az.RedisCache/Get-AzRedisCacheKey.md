---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: C0BEC701-8CE2-4B19-9F04-D32A42D9249E
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/get-azrediscachekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheKey.md
ms.openlocfilehash: 5588a3abecdec741aa6630083c38c01178669bae
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94118020"
---
# <span data-ttu-id="afaf4-101">Get-AzRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="afaf4-101">Get-AzRedisCacheKey</span></span>

## <span data-ttu-id="afaf4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="afaf4-102">SYNOPSIS</span></span>
<span data-ttu-id="afaf4-103">Obtém as teclas de acesso para um cache Redis.</span><span class="sxs-lookup"><span data-stu-id="afaf4-103">Gets the access keys for a Redis Cache.</span></span>

## <span data-ttu-id="afaf4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="afaf4-104">SYNTAX</span></span>

```
Get-AzRedisCacheKey [-ResourceGroupName <String>] -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="afaf4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="afaf4-105">DESCRIPTION</span></span>
<span data-ttu-id="afaf4-106">O cmdlet **Get-AzRedisCacheKey** Obtém as teclas de acesso para um cache do Redis do Azure.</span><span class="sxs-lookup"><span data-stu-id="afaf4-106">The **Get-AzRedisCacheKey** cmdlet gets the access keys for an Azure Redis Cache.</span></span>

## <span data-ttu-id="afaf4-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="afaf4-107">EXAMPLES</span></span>

### <span data-ttu-id="afaf4-108">Exemplo 1: obter as teclas de acesso para um cache Redis</span><span class="sxs-lookup"><span data-stu-id="afaf4-108">Example 1: Get the access keys for a Redis Cache</span></span>
```
PS C:\>Get-AzRedisCacheKey -ResourceGroupName "MyResourceGroup" -Name "MyCacheKey"
PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="afaf4-109">Esse comando obtém as teclas de acesso chamadas MyCacheKey.</span><span class="sxs-lookup"><span data-stu-id="afaf4-109">This command gets the access keys named MyCacheKey.</span></span>

## <span data-ttu-id="afaf4-110">OS</span><span class="sxs-lookup"><span data-stu-id="afaf4-110">PARAMETERS</span></span>

### <span data-ttu-id="afaf4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afaf4-111">-DefaultProfile</span></span>
<span data-ttu-id="afaf4-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="afaf4-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="afaf4-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="afaf4-113">-Name</span></span>
<span data-ttu-id="afaf4-114">Especifica o nome de um cache Redis.</span><span class="sxs-lookup"><span data-stu-id="afaf4-114">Specifies the name of a Redis Cache.</span></span>

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

### <span data-ttu-id="afaf4-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="afaf4-115">-ResourceGroupName</span></span>
<span data-ttu-id="afaf4-116">Especifica o nome do grupo de recursos que contém o cache Redis.</span><span class="sxs-lookup"><span data-stu-id="afaf4-116">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="afaf4-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afaf4-117">CommonParameters</span></span>
<span data-ttu-id="afaf4-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="afaf4-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afaf4-119">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="afaf4-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afaf4-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="afaf4-120">INPUTS</span></span>

### <span data-ttu-id="afaf4-121">System. String</span><span class="sxs-lookup"><span data-stu-id="afaf4-121">System.String</span></span>

## <span data-ttu-id="afaf4-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="afaf4-122">OUTPUTS</span></span>

### <span data-ttu-id="afaf4-123">Microsoft. Azure. Management. Redis. Models. RedisAccessKeys</span><span class="sxs-lookup"><span data-stu-id="afaf4-123">Microsoft.Azure.Management.Redis.Models.RedisAccessKeys</span></span>

## <span data-ttu-id="afaf4-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="afaf4-124">NOTES</span></span>

## <span data-ttu-id="afaf4-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="afaf4-125">RELATED LINKS</span></span>

[<span data-ttu-id="afaf4-126">New-AzRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="afaf4-126">New-AzRedisCacheKey</span></span>](./New-AzRedisCacheKey.md)


