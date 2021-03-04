---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/enable-azsecurityadvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Enable-AzSecurityAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Enable-AzSecurityAdvancedThreatProtection.md
ms.openlocfilehash: 10bda682881f35bc8401bec7304dcc1a68fd1d66
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889750"
---
# <span data-ttu-id="ec8b8-101">Enable-AzSecurityAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="ec8b8-101">Enable-AzSecurityAdvancedThreatProtection</span></span>

## <span data-ttu-id="ec8b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec8b8-102">SYNOPSIS</span></span>
<span data-ttu-id="ec8b8-103">Habilita a política avançada de proteção contra ameaças para uma conta de armazenamento /cosmosDB.</span><span class="sxs-lookup"><span data-stu-id="ec8b8-103">Enables the advanced threat protection policy for a storage / cosmosDB account.</span></span>

## <span data-ttu-id="ec8b8-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ec8b8-104">SYNTAX</span></span>

```
Enable-AzSecurityAdvancedThreatProtection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec8b8-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ec8b8-105">DESCRIPTION</span></span>
<span data-ttu-id="ec8b8-106">O `Enable-AzSecurityAdvancedThreatProtection` cmdlet habilita a política de proteção contra ameaças para uma conta de armazenamento /cosmosDB.</span><span class="sxs-lookup"><span data-stu-id="ec8b8-106">The `Enable-AzSecurityAdvancedThreatProtection` cmdlet enables the threat protection policy for a storage / cosmosDB account.</span></span>
<span data-ttu-id="ec8b8-107">Para usar esse cmdlet, especifique o *parâmetro ResourceId.*</span><span class="sxs-lookup"><span data-stu-id="ec8b8-107">To use this cmdlet, specify the *ResourceId* parameter.</span></span>

## <span data-ttu-id="ec8b8-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ec8b8-108">EXAMPLES</span></span>

### <span data-ttu-id="ec8b8-109">Exemplo 1: Conta de Armazenamento</span><span class="sxs-lookup"><span data-stu-id="ec8b8-109">Example 1: Storage Account</span></span>
```powershell
PS C:\> Enable-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"

IsEnabled Id
--------- --
    True  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"
```

<span data-ttu-id="ec8b8-110">Esse comando habilita a política avançada de proteção contra ameaças para id de `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"` recurso.</span><span class="sxs-lookup"><span data-stu-id="ec8b8-110">This command enables the advanced threat protection policy for resource id `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"`.</span></span>

### <span data-ttu-id="ec8b8-111">Exemplo 2: Conta do CosmosDB</span><span class="sxs-lookup"><span data-stu-id="ec8b8-111">Example 2: CosmosDB Account</span></span>
```powershell
PS C:\> Enable-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"

IsEnabled Id
--------- --
    True  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"
```

<span data-ttu-id="ec8b8-112">Esse comando habilita a política avançada de proteção contra ameaças para id de ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"` recurso.</span><span class="sxs-lookup"><span data-stu-id="ec8b8-112">This command enables the advanced threat protection policy for resource id ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"`.</span></span>

## <span data-ttu-id="ec8b8-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ec8b8-113">PARAMETERS</span></span>

### <span data-ttu-id="ec8b8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec8b8-114">-DefaultProfile</span></span>
<span data-ttu-id="ec8b8-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ec8b8-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec8b8-116">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ec8b8-116">-ResourceId</span></span>
<span data-ttu-id="ec8b8-117">ID do recurso de segurança em que você deseja invocar o comando.</span><span class="sxs-lookup"><span data-stu-id="ec8b8-117">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="ec8b8-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ec8b8-118">-Confirm</span></span>
<span data-ttu-id="ec8b8-119">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ec8b8-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec8b8-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec8b8-120">-WhatIf</span></span>
<span data-ttu-id="ec8b8-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ec8b8-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ec8b8-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ec8b8-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec8b8-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec8b8-123">CommonParameters</span></span>
<span data-ttu-id="ec8b8-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec8b8-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec8b8-125">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ec8b8-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec8b8-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ec8b8-126">INPUTS</span></span>

### <span data-ttu-id="ec8b8-127">Nenhum</span><span class="sxs-lookup"><span data-stu-id="ec8b8-127">None</span></span>

## <span data-ttu-id="ec8b8-128">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ec8b8-128">OUTPUTS</span></span>

### <span data-ttu-id="ec8b8-129">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="ec8b8-129">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span></span>

## <span data-ttu-id="ec8b8-130">NOTES</span><span class="sxs-lookup"><span data-stu-id="ec8b8-130">NOTES</span></span>

## <span data-ttu-id="ec8b8-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ec8b8-131">RELATED LINKS</span></span>
