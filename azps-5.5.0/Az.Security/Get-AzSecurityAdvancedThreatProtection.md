---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/get-azsecurityadvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdvancedThreatProtection.md
ms.openlocfilehash: e4412d770f47bda0de735b315d638c0b8fdb26df
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118718"
---
# <span data-ttu-id="c4a01-101">Get-AzSecurityAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="c4a01-101">Get-AzSecurityAdvancedThreatProtection</span></span>

## <span data-ttu-id="c4a01-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c4a01-102">SYNOPSIS</span></span>
<span data-ttu-id="c4a01-103">Obtém a política avançada de proteção contra ameaças para uma conta de armazenamento /cosmosDB.</span><span class="sxs-lookup"><span data-stu-id="c4a01-103">Gets the advanced threat protection policy for a storage / cosmosDB account.</span></span>

## <span data-ttu-id="c4a01-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c4a01-104">SYNTAX</span></span>

```
Get-AzSecurityAdvancedThreatProtection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c4a01-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="c4a01-105">DESCRIPTION</span></span>
<span data-ttu-id="c4a01-106">O `Get-AzSecurityAdvancedThreatProtection` cmdlet obtém a política de proteção contra ameaças para uma conta de armazenamento/xpDB.</span><span class="sxs-lookup"><span data-stu-id="c4a01-106">The `Get-AzSecurityAdvancedThreatProtection` cmdlet gets the threat protection policy for a storage / cosmosDB account.</span></span>
<span data-ttu-id="c4a01-107">Para usar esse cmdlet, especifique o *parâmetro ResourceId.*</span><span class="sxs-lookup"><span data-stu-id="c4a01-107">To use this cmdlet, specify the *ResourceId* parameter.</span></span>

## <span data-ttu-id="c4a01-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c4a01-108">EXAMPLES</span></span>

### <span data-ttu-id="c4a01-109">Exemplo 1: Conta de Armazenamento</span><span class="sxs-lookup"><span data-stu-id="c4a01-109">Example 1: Storage Account</span></span>
```powershell
PS C:\> Get-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"

IsEnabled Id
--------- --
    False  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"
```

<span data-ttu-id="c4a01-110">Esse comando obtém a política avançada de proteção contra ameaças para a ID do `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"` recurso.</span><span class="sxs-lookup"><span data-stu-id="c4a01-110">This command gets the advanced threat protection policy for resource id `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"`.</span></span>

### <span data-ttu-id="c4a01-111">Exemplo 2: Conta do XpDB</span><span class="sxs-lookup"><span data-stu-id="c4a01-111">Example 2: CosmosDB Account</span></span>
```powershell
PS C:\> Get-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"

IsEnabled Id
--------- --
    True  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"
```

<span data-ttu-id="c4a01-112">Esse comando obtém a política avançada de proteção contra ameaças para a ID do ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"` recurso.</span><span class="sxs-lookup"><span data-stu-id="c4a01-112">This command gets the advanced threat protection policy for resource id ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"`.</span></span>

## <span data-ttu-id="c4a01-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c4a01-113">PARAMETERS</span></span>

### <span data-ttu-id="c4a01-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4a01-114">-DefaultProfile</span></span>
<span data-ttu-id="c4a01-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c4a01-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4a01-116">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c4a01-116">-ResourceId</span></span>
<span data-ttu-id="c4a01-117">ID do recurso de segurança em que você deseja invocar o comando.</span><span class="sxs-lookup"><span data-stu-id="c4a01-117">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="c4a01-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4a01-118">CommonParameters</span></span>
<span data-ttu-id="c4a01-119">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4a01-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4a01-120">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c4a01-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4a01-121">Entradas</span><span class="sxs-lookup"><span data-stu-id="c4a01-121">INPUTS</span></span>

### <span data-ttu-id="c4a01-122">System.String</span><span class="sxs-lookup"><span data-stu-id="c4a01-122">System.String</span></span>

## <span data-ttu-id="c4a01-123">Saídas</span><span class="sxs-lookup"><span data-stu-id="c4a01-123">OUTPUTS</span></span>

### <span data-ttu-id="c4a01-124">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="c4a01-124">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span></span>

## <span data-ttu-id="c4a01-125">Notas</span><span class="sxs-lookup"><span data-stu-id="c4a01-125">NOTES</span></span>

## <span data-ttu-id="c4a01-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c4a01-126">RELATED LINKS</span></span>
