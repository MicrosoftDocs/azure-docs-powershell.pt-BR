---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/get-azsecurityadvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdvancedThreatProtection.md
ms.openlocfilehash: 13ab536d08de0092523f860defe04a6e973d90e8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772510"
---
# <span data-ttu-id="0a881-101">Get-AzSecurityAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="0a881-101">Get-AzSecurityAdvancedThreatProtection</span></span>

## <span data-ttu-id="0a881-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0a881-102">SYNOPSIS</span></span>
<span data-ttu-id="0a881-103">Obtém a política avançada de proteção contra ameaças para uma conta de armazenamento/cosmosDB.</span><span class="sxs-lookup"><span data-stu-id="0a881-103">Gets the advanced threat protection policy for a storage / cosmosDB account.</span></span>

## <span data-ttu-id="0a881-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0a881-104">SYNTAX</span></span>

```
Get-AzSecurityAdvancedThreatProtection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0a881-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0a881-105">DESCRIPTION</span></span>
<span data-ttu-id="0a881-106">O `Get-AzSecurityAdvancedThreatProtection` cmdlet obtém a política de proteção contra ameaças para uma conta de armazenamento/cosmosDB.</span><span class="sxs-lookup"><span data-stu-id="0a881-106">The `Get-AzSecurityAdvancedThreatProtection` cmdlet gets the threat protection policy for a storage / cosmosDB account.</span></span>
<span data-ttu-id="0a881-107">Para usar esse cmdlet, especifique o parâmetro *ResourceId* .</span><span class="sxs-lookup"><span data-stu-id="0a881-107">To use this cmdlet, specify the *ResourceId* parameter.</span></span>

## <span data-ttu-id="0a881-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0a881-108">EXAMPLES</span></span>

### <span data-ttu-id="0a881-109">Exemplo 1: conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="0a881-109">Example 1 : Storage Account</span></span>
```powershell
PS C:\> Get-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"

IsEnabled Id
--------- --
    False  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"
```

<span data-ttu-id="0a881-110">Este comando obtém a política avançada de proteção contra ameaças para a ID do recurso `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"` .</span><span class="sxs-lookup"><span data-stu-id="0a881-110">This command gets the advanced threat protection policy for resource id `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"`.</span></span>

### <span data-ttu-id="0a881-111">Exemplo 2: conta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="0a881-111">Example 2 : CosmosDB Account</span></span>
```powershell
PS C:\> Get-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"

IsEnabled Id
--------- --
    True  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"
```
<span data-ttu-id="0a881-112">Este comando obtém a política avançada de proteção contra ameaças para a ID do recurso ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"` .</span><span class="sxs-lookup"><span data-stu-id="0a881-112">This command gets the advanced threat protection policy for resource id ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"`.</span></span>


## <span data-ttu-id="0a881-113">OS</span><span class="sxs-lookup"><span data-stu-id="0a881-113">PARAMETERS</span></span>

### <span data-ttu-id="0a881-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a881-114">-DefaultProfile</span></span>
<span data-ttu-id="0a881-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0a881-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a881-116">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0a881-116">-ResourceId</span></span>
<span data-ttu-id="0a881-117">ID do recurso de segurança no qual você deseja invocar o comando.</span><span class="sxs-lookup"><span data-stu-id="0a881-117">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="0a881-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a881-118">CommonParameters</span></span>
<span data-ttu-id="0a881-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a881-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a881-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a881-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a881-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0a881-121">INPUTS</span></span>

### <span data-ttu-id="0a881-122">System. String</span><span class="sxs-lookup"><span data-stu-id="0a881-122">System.String</span></span>

## <span data-ttu-id="0a881-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0a881-123">OUTPUTS</span></span>

### <span data-ttu-id="0a881-124">Microsoft. Azure. Commands. Security. Models. AdvancedThreatProtection. PSAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="0a881-124">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span></span>

## <span data-ttu-id="0a881-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0a881-125">NOTES</span></span>

## <span data-ttu-id="0a881-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0a881-126">RELATED LINKS</span></span>