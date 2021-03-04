---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 1F86CE62-AA01-44FB-A935-484EC51DDE5A
online version: https://docs.microsoft.com/powershell/module/az.rediscache/new-azrediscachekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheKey.md
ms.openlocfilehash: 1d9b11aa7c259a3534b76a1d1ef011671c7f1142
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901441"
---
# <span data-ttu-id="98f1e-101">New-AzRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="98f1e-101">New-AzRedisCacheKey</span></span>

## <span data-ttu-id="98f1e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="98f1e-102">SYNOPSIS</span></span>
<span data-ttu-id="98f1e-103">Regenera a chave de acesso de um Cache Redis.</span><span class="sxs-lookup"><span data-stu-id="98f1e-103">Regenerates the access key of a Redis Cache.</span></span>

## <span data-ttu-id="98f1e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="98f1e-104">SYNTAX</span></span>

```
New-AzRedisCacheKey [-ResourceGroupName <String>] -Name <String> -KeyType <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98f1e-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="98f1e-105">DESCRIPTION</span></span>
<span data-ttu-id="98f1e-106">O cmdlet **New-AzRedisCacheKey** regenera a chave de acesso de um Cache do Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="98f1e-106">The **New-AzRedisCacheKey** cmdlet regenerates the access key of an Azure Redis Cache.</span></span>

## <span data-ttu-id="98f1e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="98f1e-107">EXAMPLES</span></span>

### <span data-ttu-id="98f1e-108">Exemplo 1: Regenerar uma chave primária</span><span class="sxs-lookup"><span data-stu-id="98f1e-108">Example 1: Regenerate a primary key</span></span>
```
PS C:\>New-AzRedisCacheKey -ResourceGroupName "ResourceGroup03" -Name "myCache" -KeyType "Primary" -Force

          PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=

          SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="98f1e-109">Este comando regenera a chave primária de um Cache Redis.</span><span class="sxs-lookup"><span data-stu-id="98f1e-109">This command regenerates the primary key of a Redis Cache.</span></span>

### <span data-ttu-id="98f1e-110">Exemplo 2: Regenerar uma chave secundária</span><span class="sxs-lookup"><span data-stu-id="98f1e-110">Example 2: Regenerate a secondary key</span></span>
```
PS C:\>New-AzRedisCacheKey -ResourceGroupName "ResourceGroup03" -Name "myCache" -KeyType "Secondary" -Force
          PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=

          SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="98f1e-111">Este comando regenera a chave secundária de um Cache Redis.</span><span class="sxs-lookup"><span data-stu-id="98f1e-111">This command regenerates the secondary key of a Redis Cache.</span></span>

## <span data-ttu-id="98f1e-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="98f1e-112">PARAMETERS</span></span>

### <span data-ttu-id="98f1e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98f1e-113">-DefaultProfile</span></span>
<span data-ttu-id="98f1e-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="98f1e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="98f1e-115">-Force</span><span class="sxs-lookup"><span data-stu-id="98f1e-115">-Force</span></span>
<span data-ttu-id="98f1e-116">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="98f1e-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98f1e-117">-KeyType</span><span class="sxs-lookup"><span data-stu-id="98f1e-117">-KeyType</span></span>
<span data-ttu-id="98f1e-118">Especifica se a chave de acesso primária ou secundária deve ser regenerada.</span><span class="sxs-lookup"><span data-stu-id="98f1e-118">Specifies whether to regenerate the primary or secondary access key.</span></span>
<span data-ttu-id="98f1e-119">Os valores válidos são: Primário, Secundário.</span><span class="sxs-lookup"><span data-stu-id="98f1e-119">Valid values are: Primary, Secondary.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98f1e-120">-Name</span><span class="sxs-lookup"><span data-stu-id="98f1e-120">-Name</span></span>
<span data-ttu-id="98f1e-121">Especifica o nome do Cache Redis.</span><span class="sxs-lookup"><span data-stu-id="98f1e-121">Specifies the name of the Redis Cache.</span></span>

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

### <span data-ttu-id="98f1e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98f1e-122">-ResourceGroupName</span></span>
<span data-ttu-id="98f1e-123">Especifica o nome do grupo de recursos que contém o Cache Redis.</span><span class="sxs-lookup"><span data-stu-id="98f1e-123">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="98f1e-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="98f1e-124">-Confirm</span></span>
<span data-ttu-id="98f1e-125">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98f1e-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98f1e-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98f1e-126">-WhatIf</span></span>
<span data-ttu-id="98f1e-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="98f1e-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98f1e-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="98f1e-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98f1e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98f1e-129">CommonParameters</span></span>
<span data-ttu-id="98f1e-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98f1e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98f1e-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98f1e-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98f1e-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="98f1e-132">INPUTS</span></span>

### <span data-ttu-id="98f1e-133">System.String</span><span class="sxs-lookup"><span data-stu-id="98f1e-133">System.String</span></span>

## <span data-ttu-id="98f1e-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="98f1e-134">OUTPUTS</span></span>

### <span data-ttu-id="98f1e-135">Microsoft.Azure.Management.Redis.Models.RedisAccessKeys</span><span class="sxs-lookup"><span data-stu-id="98f1e-135">Microsoft.Azure.Management.Redis.Models.RedisAccessKeys</span></span>

## <span data-ttu-id="98f1e-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="98f1e-136">NOTES</span></span>

## <span data-ttu-id="98f1e-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="98f1e-137">RELATED LINKS</span></span>

[<span data-ttu-id="98f1e-138">Get-AzRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="98f1e-138">Get-AzRedisCacheKey</span></span>](./Get-AzRedisCacheKey.md)


