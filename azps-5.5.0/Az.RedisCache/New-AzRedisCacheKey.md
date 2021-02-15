---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 1F86CE62-AA01-44FB-A935-484EC51DDE5A
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscachekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheKey.md
ms.openlocfilehash: f48d49a59b21cbae3f314926f4de92e74a2b10e8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118174"
---
# <span data-ttu-id="7d239-101">New-AzRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="7d239-101">New-AzRedisCacheKey</span></span>

## <span data-ttu-id="7d239-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7d239-102">SYNOPSIS</span></span>
<span data-ttu-id="7d239-103">Regenera a chave de acesso de um Cache de Redis.</span><span class="sxs-lookup"><span data-stu-id="7d239-103">Regenerates the access key of a Redis Cache.</span></span>

## <span data-ttu-id="7d239-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7d239-104">SYNTAX</span></span>

```
New-AzRedisCacheKey [-ResourceGroupName <String>] -Name <String> -KeyType <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d239-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="7d239-105">DESCRIPTION</span></span>
<span data-ttu-id="7d239-106">O cmdlet **New-AzRedisCacheKey** regenera a chave de acesso de um Cache de Redis do Azure.</span><span class="sxs-lookup"><span data-stu-id="7d239-106">The **New-AzRedisCacheKey** cmdlet regenerates the access key of an Azure Redis Cache.</span></span>

## <span data-ttu-id="7d239-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7d239-107">EXAMPLES</span></span>

### <span data-ttu-id="7d239-108">Exemplo 1: Regenerar uma chave primária</span><span class="sxs-lookup"><span data-stu-id="7d239-108">Example 1: Regenerate a primary key</span></span>
```
PS C:\>New-AzRedisCacheKey -ResourceGroupName "ResourceGroup03" -Name "myCache" -KeyType "Primary" -Force

          PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=

          SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="7d239-109">Esse comando regenera a chave primária de um Cache de Redis.</span><span class="sxs-lookup"><span data-stu-id="7d239-109">This command regenerates the primary key of a Redis Cache.</span></span>

### <span data-ttu-id="7d239-110">Exemplo 2: Regenerar uma chave secundária</span><span class="sxs-lookup"><span data-stu-id="7d239-110">Example 2: Regenerate a secondary key</span></span>
```
PS C:\>New-AzRedisCacheKey -ResourceGroupName "ResourceGroup03" -Name "myCache" -KeyType "Secondary" -Force
          PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=

          SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="7d239-111">Esse comando regenera a chave secundária de um Cache de Redis.</span><span class="sxs-lookup"><span data-stu-id="7d239-111">This command regenerates the secondary key of a Redis Cache.</span></span>

## <span data-ttu-id="7d239-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7d239-112">PARAMETERS</span></span>

### <span data-ttu-id="7d239-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d239-113">-DefaultProfile</span></span>
<span data-ttu-id="7d239-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="7d239-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d239-115">-Forçar</span><span class="sxs-lookup"><span data-stu-id="7d239-115">-Force</span></span>
<span data-ttu-id="7d239-116">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="7d239-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7d239-117">-KeyType</span><span class="sxs-lookup"><span data-stu-id="7d239-117">-KeyType</span></span>
<span data-ttu-id="7d239-118">Especifica se a chave de acesso principal ou secundária deve ser regenerada.</span><span class="sxs-lookup"><span data-stu-id="7d239-118">Specifies whether to regenerate the primary or secondary access key.</span></span>
<span data-ttu-id="7d239-119">Os valores válidos são: Principal, Secundário.</span><span class="sxs-lookup"><span data-stu-id="7d239-119">Valid values are: Primary, Secondary.</span></span>

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

### <span data-ttu-id="7d239-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="7d239-120">-Name</span></span>
<span data-ttu-id="7d239-121">Especifica o nome do Cache de Redis.</span><span class="sxs-lookup"><span data-stu-id="7d239-121">Specifies the name of the Redis Cache.</span></span>

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

### <span data-ttu-id="7d239-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d239-122">-ResourceGroupName</span></span>
<span data-ttu-id="7d239-123">Especifica o nome do grupo de recursos que contém o Cache de Redis.</span><span class="sxs-lookup"><span data-stu-id="7d239-123">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="7d239-124">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="7d239-124">-Confirm</span></span>
<span data-ttu-id="7d239-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7d239-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d239-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d239-126">-WhatIf</span></span>
<span data-ttu-id="7d239-127">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="7d239-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d239-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7d239-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d239-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d239-129">CommonParameters</span></span>
<span data-ttu-id="7d239-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d239-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d239-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d239-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d239-132">Entradas</span><span class="sxs-lookup"><span data-stu-id="7d239-132">INPUTS</span></span>

### <span data-ttu-id="7d239-133">System.String</span><span class="sxs-lookup"><span data-stu-id="7d239-133">System.String</span></span>

## <span data-ttu-id="7d239-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="7d239-134">OUTPUTS</span></span>

### <span data-ttu-id="7d239-135">Microsoft.Azure.Management.Redis.Models.RedisAccessKeys</span><span class="sxs-lookup"><span data-stu-id="7d239-135">Microsoft.Azure.Management.Redis.Models.RedisAccessKeys</span></span>

## <span data-ttu-id="7d239-136">Notas</span><span class="sxs-lookup"><span data-stu-id="7d239-136">NOTES</span></span>

## <span data-ttu-id="7d239-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7d239-137">RELATED LINKS</span></span>

[<span data-ttu-id="7d239-138">Get-AzRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="7d239-138">Get-AzRedisCacheKey</span></span>](./Get-AzRedisCacheKey.md)


