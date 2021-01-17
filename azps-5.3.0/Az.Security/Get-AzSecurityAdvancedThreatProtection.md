---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/get-azsecurityadvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdvancedThreatProtection.md
ms.openlocfilehash: e4412d770f47bda0de735b315d638c0b8fdb26df
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433287"
---
# <span data-ttu-id="e4811-101">Get-AzSecurityAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="e4811-101">Get-AzSecurityAdvancedThreatProtection</span></span>

## <span data-ttu-id="e4811-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e4811-102">SYNOPSIS</span></span>
<span data-ttu-id="e4811-103">Obtém a política avançada de proteção contra ameaças para uma conta de armazenamento/cosmosDB.</span><span class="sxs-lookup"><span data-stu-id="e4811-103">Gets the advanced threat protection policy for a storage / cosmosDB account.</span></span>

## <span data-ttu-id="e4811-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e4811-104">SYNTAX</span></span>

```
Get-AzSecurityAdvancedThreatProtection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e4811-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e4811-105">DESCRIPTION</span></span>
<span data-ttu-id="e4811-106">O `Get-AzSecurityAdvancedThreatProtection` cmdlet obtém a política de proteção contra ameaças para uma conta de armazenamento/cosmosDB.</span><span class="sxs-lookup"><span data-stu-id="e4811-106">The `Get-AzSecurityAdvancedThreatProtection` cmdlet gets the threat protection policy for a storage / cosmosDB account.</span></span>
<span data-ttu-id="e4811-107">Para usar esse cmdlet, especifique o parâmetro *ResourceId* .</span><span class="sxs-lookup"><span data-stu-id="e4811-107">To use this cmdlet, specify the *ResourceId* parameter.</span></span>

## <span data-ttu-id="e4811-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e4811-108">EXAMPLES</span></span>

### <span data-ttu-id="e4811-109">Exemplo 1: conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="e4811-109">Example 1: Storage Account</span></span>
```powershell
PS C:\> Get-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"

IsEnabled Id
--------- --
    False  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"
```

<span data-ttu-id="e4811-110">Este comando obtém a política avançada de proteção contra ameaças para a ID do recurso `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"` .</span><span class="sxs-lookup"><span data-stu-id="e4811-110">This command gets the advanced threat protection policy for resource id `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"`.</span></span>

### <span data-ttu-id="e4811-111">Exemplo 2: conta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="e4811-111">Example 2: CosmosDB Account</span></span>
```powershell
PS C:\> Get-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"

IsEnabled Id
--------- --
    True  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"
```

<span data-ttu-id="e4811-112">Este comando obtém a política avançada de proteção contra ameaças para a ID do recurso ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"` .</span><span class="sxs-lookup"><span data-stu-id="e4811-112">This command gets the advanced threat protection policy for resource id ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"`.</span></span>

## <span data-ttu-id="e4811-113">OS</span><span class="sxs-lookup"><span data-stu-id="e4811-113">PARAMETERS</span></span>

### <span data-ttu-id="e4811-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4811-114">-DefaultProfile</span></span>
<span data-ttu-id="e4811-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e4811-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4811-116">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e4811-116">-ResourceId</span></span>
<span data-ttu-id="e4811-117">ID do recurso de segurança no qual você deseja invocar o comando.</span><span class="sxs-lookup"><span data-stu-id="e4811-117">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="e4811-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4811-118">CommonParameters</span></span>
<span data-ttu-id="e4811-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4811-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4811-120">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e4811-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4811-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e4811-121">INPUTS</span></span>

### <span data-ttu-id="e4811-122">System. String</span><span class="sxs-lookup"><span data-stu-id="e4811-122">System.String</span></span>

## <span data-ttu-id="e4811-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e4811-123">OUTPUTS</span></span>

### <span data-ttu-id="e4811-124">Microsoft. Azure. Commands. Security. Models. AdvancedThreatProtection. PSAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="e4811-124">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span></span>

## <span data-ttu-id="e4811-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e4811-125">NOTES</span></span>

## <span data-ttu-id="e4811-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e4811-126">RELATED LINKS</span></span>
