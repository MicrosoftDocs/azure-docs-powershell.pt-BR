---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/get-azredisenterprisecachedatabasekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCacheDatabaseKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCacheDatabaseKey.md
ms.openlocfilehash: e602cb4fc86ede6a4e1f7cc894c1825fd1d560fb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112661"
---
# <span data-ttu-id="a1c9d-101">Get-AzRedisEnterpriseCacheDatabaseKey</span><span class="sxs-lookup"><span data-stu-id="a1c9d-101">Get-AzRedisEnterpriseCacheDatabaseKey</span></span>

## <span data-ttu-id="a1c9d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a1c9d-102">SYNOPSIS</span></span>
<span data-ttu-id="a1c9d-103">Recupera as teclas de acesso do banco de dados RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="a1c9d-103">Retrieves the access keys for the RedisEnterprise database.</span></span>

## <span data-ttu-id="a1c9d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a1c9d-104">SYNTAX</span></span>

```
Get-AzRedisEnterpriseCacheDatabaseKey -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a1c9d-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="a1c9d-105">DESCRIPTION</span></span>
<span data-ttu-id="a1c9d-106">Recupera as teclas de acesso do banco de dados RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="a1c9d-106">Retrieves the access keys for the RedisEnterprise database.</span></span>

## <span data-ttu-id="a1c9d-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a1c9d-107">EXAMPLES</span></span>

### <span data-ttu-id="a1c9d-108">Exemplo 1: Obter chaves de acesso ao banco de dados</span><span class="sxs-lookup"><span data-stu-id="a1c9d-108">Example 1: Get database access keys</span></span>
```powershell
PS C:\> Get-AzRedisEnterpriseCacheDatabaseKey -Name "MyCache" -ResourceGroupName "MyGroup"

PrimaryKey                                   SecondaryKey
----------                                   ------------
primary-key                                  secondary-key

```

<span data-ttu-id="a1c9d-109">Esse comando obtém as chaves de acesso secretas usadas para autenticar conexões com o banco de dados do Cache Corporativo Redis chamado MyCache.</span><span class="sxs-lookup"><span data-stu-id="a1c9d-109">This command gets the secret access keys used for authenticating connections to the database of the Redis Enterprise Cache named MyCache.</span></span>

## <span data-ttu-id="a1c9d-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a1c9d-110">PARAMETERS</span></span>

### <span data-ttu-id="a1c9d-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="a1c9d-111">-ClusterName</span></span>
<span data-ttu-id="a1c9d-112">O nome do cluster RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="a1c9d-112">The name of the RedisEnterprise cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1c9d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1c9d-113">-DefaultProfile</span></span>
<span data-ttu-id="a1c9d-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a1c9d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1c9d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1c9d-115">-ResourceGroupName</span></span>
<span data-ttu-id="a1c9d-116">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a1c9d-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="a1c9d-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a1c9d-117">-SubscriptionId</span></span>
<span data-ttu-id="a1c9d-118">Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a1c9d-118">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="a1c9d-119">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="a1c9d-119">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1c9d-120">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="a1c9d-120">-Confirm</span></span>
<span data-ttu-id="a1c9d-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1c9d-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1c9d-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1c9d-122">-WhatIf</span></span>
<span data-ttu-id="a1c9d-123">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="a1c9d-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1c9d-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a1c9d-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1c9d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1c9d-125">CommonParameters</span></span>
<span data-ttu-id="a1c9d-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1c9d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1c9d-127">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a1c9d-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1c9d-128">Entradas</span><span class="sxs-lookup"><span data-stu-id="a1c9d-128">INPUTS</span></span>

## <span data-ttu-id="a1c9d-129">Saídas</span><span class="sxs-lookup"><span data-stu-id="a1c9d-129">OUTPUTS</span></span>

### <span data-ttu-id="a1c9d-130">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IAccessKeys</span><span class="sxs-lookup"><span data-stu-id="a1c9d-130">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IAccessKeys</span></span>

## <span data-ttu-id="a1c9d-131">Notas</span><span class="sxs-lookup"><span data-stu-id="a1c9d-131">NOTES</span></span>

<span data-ttu-id="a1c9d-132">Aliases</span><span class="sxs-lookup"><span data-stu-id="a1c9d-132">ALIASES</span></span>

## <span data-ttu-id="a1c9d-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a1c9d-133">RELATED LINKS</span></span>

