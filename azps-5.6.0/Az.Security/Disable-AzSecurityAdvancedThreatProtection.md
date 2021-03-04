---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/disable-azsecurityadvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Disable-AzSecurityAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Disable-AzSecurityAdvancedThreatProtection.md
ms.openlocfilehash: ed59b77a934787b1030166b24e9ed3af81698c16
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889751"
---
# <span data-ttu-id="d3e55-101">Disable-AzSecurityAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="d3e55-101">Disable-AzSecurityAdvancedThreatProtection</span></span>

## <span data-ttu-id="d3e55-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3e55-102">SYNOPSIS</span></span>
<span data-ttu-id="d3e55-103">Desabilita a política avançada de proteção contra ameaças para uma conta de armazenamento /cosmosDB.</span><span class="sxs-lookup"><span data-stu-id="d3e55-103">Disables the advanced threat protection policy for a storage / cosmosDB account.</span></span>

## <span data-ttu-id="d3e55-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d3e55-104">SYNTAX</span></span>

```
Disable-AzSecurityAdvancedThreatProtection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3e55-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d3e55-105">DESCRIPTION</span></span>
<span data-ttu-id="d3e55-106">O `Disable-AzSecurityAdvancedThreatProtection` cmdlet desabilita a política de proteção contra ameaças para uma conta de armazenamento /cosmosDB.</span><span class="sxs-lookup"><span data-stu-id="d3e55-106">The `Disable-AzSecurityAdvancedThreatProtection` cmdlet disables the threat protection policy for a storage / cosmosDB account.</span></span>
<span data-ttu-id="d3e55-107">Para usar esse cmdlet, especifique o *parâmetro ResourceId.*</span><span class="sxs-lookup"><span data-stu-id="d3e55-107">To use this cmdlet, specify the *ResourceId* parameter.</span></span>

## <span data-ttu-id="d3e55-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d3e55-108">EXAMPLES</span></span>

### <span data-ttu-id="d3e55-109">Exemplo 1 : Conta de Armazenamento</span><span class="sxs-lookup"><span data-stu-id="d3e55-109">Example 1 : Storage Account</span></span>
```powershell
PS C:\> Disable-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"

IsEnabled Id
--------- --
    False  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"
```

<span data-ttu-id="d3e55-110">Este comando desabilita a política avançada de proteção contra ameaças para id de `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"` recurso.</span><span class="sxs-lookup"><span data-stu-id="d3e55-110">This command disables the advanced threat protection policy for resource id `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"`.</span></span>

### <span data-ttu-id="d3e55-111">Exemplo 2 : Conta do CosmosDB</span><span class="sxs-lookup"><span data-stu-id="d3e55-111">Example 2 : CosmosDB Account</span></span>
```powershell
PS C:\> Disable-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"

IsEnabled Id
--------- --
    False  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"
```

<span data-ttu-id="d3e55-112">Este comando desabilita a política avançada de proteção contra ameaças para id de ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"` recurso.</span><span class="sxs-lookup"><span data-stu-id="d3e55-112">This command disables the advanced threat protection policy for resource id ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"`.</span></span>

## <span data-ttu-id="d3e55-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d3e55-113">PARAMETERS</span></span>

### <span data-ttu-id="d3e55-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3e55-114">-DefaultProfile</span></span>
<span data-ttu-id="d3e55-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d3e55-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3e55-116">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d3e55-116">-ResourceId</span></span>
<span data-ttu-id="d3e55-117">ID do recurso de segurança em que você deseja invocar o comando.</span><span class="sxs-lookup"><span data-stu-id="d3e55-117">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="d3e55-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d3e55-118">-Confirm</span></span>
<span data-ttu-id="d3e55-119">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d3e55-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3e55-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3e55-120">-WhatIf</span></span>
<span data-ttu-id="d3e55-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d3e55-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d3e55-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d3e55-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3e55-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3e55-123">CommonParameters</span></span>
<span data-ttu-id="d3e55-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3e55-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3e55-125">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d3e55-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3e55-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d3e55-126">INPUTS</span></span>

### <span data-ttu-id="d3e55-127">Nenhum</span><span class="sxs-lookup"><span data-stu-id="d3e55-127">None</span></span>

## <span data-ttu-id="d3e55-128">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d3e55-128">OUTPUTS</span></span>

### <span data-ttu-id="d3e55-129">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="d3e55-129">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span></span>

## <span data-ttu-id="d3e55-130">NOTES</span><span class="sxs-lookup"><span data-stu-id="d3e55-130">NOTES</span></span>

## <span data-ttu-id="d3e55-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d3e55-131">RELATED LINKS</span></span>
