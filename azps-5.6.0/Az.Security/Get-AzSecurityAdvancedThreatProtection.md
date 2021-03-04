---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/get-azsecurityadvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdvancedThreatProtection.md
ms.openlocfilehash: ec35304bf6c376747fa6f98e7fb5753293e579b7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892721"
---
# <span data-ttu-id="f7984-101">Get-AzSecurityAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="f7984-101">Get-AzSecurityAdvancedThreatProtection</span></span>

## <span data-ttu-id="f7984-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7984-102">SYNOPSIS</span></span>
<span data-ttu-id="f7984-103">Obtém a política avançada de proteção contra ameaças para uma conta de armazenamento /cosmosDB.</span><span class="sxs-lookup"><span data-stu-id="f7984-103">Gets the advanced threat protection policy for a storage / cosmosDB account.</span></span>

## <span data-ttu-id="f7984-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f7984-104">SYNTAX</span></span>

```
Get-AzSecurityAdvancedThreatProtection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f7984-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f7984-105">DESCRIPTION</span></span>
<span data-ttu-id="f7984-106">O `Get-AzSecurityAdvancedThreatProtection` cmdlet obtém a política de proteção contra ameaças para uma conta de armazenamento /cosmosDB.</span><span class="sxs-lookup"><span data-stu-id="f7984-106">The `Get-AzSecurityAdvancedThreatProtection` cmdlet gets the threat protection policy for a storage / cosmosDB account.</span></span>
<span data-ttu-id="f7984-107">Para usar esse cmdlet, especifique o *parâmetro ResourceId.*</span><span class="sxs-lookup"><span data-stu-id="f7984-107">To use this cmdlet, specify the *ResourceId* parameter.</span></span>

## <span data-ttu-id="f7984-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f7984-108">EXAMPLES</span></span>

### <span data-ttu-id="f7984-109">Exemplo 1: Conta de Armazenamento</span><span class="sxs-lookup"><span data-stu-id="f7984-109">Example 1: Storage Account</span></span>
```powershell
PS C:\> Get-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"

IsEnabled Id
--------- --
    False  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"
```

<span data-ttu-id="f7984-110">Este comando obtém a política avançada de proteção contra ameaças para id de `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"` recurso.</span><span class="sxs-lookup"><span data-stu-id="f7984-110">This command gets the advanced threat protection policy for resource id `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"`.</span></span>

### <span data-ttu-id="f7984-111">Exemplo 2: Conta do CosmosDB</span><span class="sxs-lookup"><span data-stu-id="f7984-111">Example 2: CosmosDB Account</span></span>
```powershell
PS C:\> Get-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"

IsEnabled Id
--------- --
    True  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"
```

<span data-ttu-id="f7984-112">Este comando obtém a política avançada de proteção contra ameaças para id de ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"` recurso.</span><span class="sxs-lookup"><span data-stu-id="f7984-112">This command gets the advanced threat protection policy for resource id ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"`.</span></span>

## <span data-ttu-id="f7984-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f7984-113">PARAMETERS</span></span>

### <span data-ttu-id="f7984-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7984-114">-DefaultProfile</span></span>
<span data-ttu-id="f7984-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f7984-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7984-116">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f7984-116">-ResourceId</span></span>
<span data-ttu-id="f7984-117">ID do recurso de segurança em que você deseja invocar o comando.</span><span class="sxs-lookup"><span data-stu-id="f7984-117">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="f7984-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7984-118">CommonParameters</span></span>
<span data-ttu-id="f7984-119">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7984-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7984-120">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f7984-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7984-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f7984-121">INPUTS</span></span>

### <span data-ttu-id="f7984-122">System.String</span><span class="sxs-lookup"><span data-stu-id="f7984-122">System.String</span></span>

## <span data-ttu-id="f7984-123">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f7984-123">OUTPUTS</span></span>

### <span data-ttu-id="f7984-124">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="f7984-124">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span></span>

## <span data-ttu-id="f7984-125">NOTES</span><span class="sxs-lookup"><span data-stu-id="f7984-125">NOTES</span></span>

## <span data-ttu-id="f7984-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f7984-126">RELATED LINKS</span></span>
