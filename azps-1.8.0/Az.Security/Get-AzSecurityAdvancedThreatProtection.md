---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/get-azsecurityadvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdvancedThreatProtection.md
ms.openlocfilehash: 8957a794660750f45f295b77d921e647d368e7dc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599258"
---
# <span data-ttu-id="ed479-101">Get-AzSecurityAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="ed479-101">Get-AzSecurityAdvancedThreatProtection</span></span>

## <span data-ttu-id="ed479-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ed479-102">SYNOPSIS</span></span>
<span data-ttu-id="ed479-103">Obtém a política avançada de proteção contra ameaças para uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="ed479-103">Gets the advanced threat protection policy for a storage account.</span></span>

## <span data-ttu-id="ed479-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ed479-104">SYNTAX</span></span>

```
Get-AzSecurityAdvancedThreatProtection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ed479-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ed479-105">DESCRIPTION</span></span>
<span data-ttu-id="ed479-106">O `Get-AzSecurityAdvancedThreatProtection` cmdlet obtém a política de proteção contra ameaças para uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="ed479-106">The `Get-AzSecurityAdvancedThreatProtection` cmdlet gets the threat protection policy for a storage account.</span></span>
<span data-ttu-id="ed479-107">Para usar esse cmdlet, especifique o parâmetro *ResourceId* .</span><span class="sxs-lookup"><span data-stu-id="ed479-107">To use this cmdlet, specify the *ResourceId* parameter.</span></span>

## <span data-ttu-id="ed479-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ed479-108">EXAMPLES</span></span>

### <span data-ttu-id="ed479-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ed479-109">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"

IsEnabled Id
--------- --
    False  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"
```

<span data-ttu-id="ed479-110">Este comando obtém a política avançada de proteção contra ameaças para a ID do recurso `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"` .</span><span class="sxs-lookup"><span data-stu-id="ed479-110">This command gets the advanced threat protection policy for resource id `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"`.</span></span>

## <span data-ttu-id="ed479-111">OS</span><span class="sxs-lookup"><span data-stu-id="ed479-111">PARAMETERS</span></span>

### <span data-ttu-id="ed479-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed479-112">-DefaultProfile</span></span>
<span data-ttu-id="ed479-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ed479-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed479-114">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ed479-114">-ResourceId</span></span>
<span data-ttu-id="ed479-115">ID do recurso de segurança no qual você deseja invocar o comando.</span><span class="sxs-lookup"><span data-stu-id="ed479-115">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="ed479-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed479-116">CommonParameters</span></span>
<span data-ttu-id="ed479-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed479-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed479-118">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed479-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed479-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ed479-119">INPUTS</span></span>

### <span data-ttu-id="ed479-120">System. String</span><span class="sxs-lookup"><span data-stu-id="ed479-120">System.String</span></span>

## <span data-ttu-id="ed479-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ed479-121">OUTPUTS</span></span>

### <span data-ttu-id="ed479-122">Microsoft. Azure. Commands. Security. Models. AdvancedThreatProtection. PSAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="ed479-122">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span></span>

## <span data-ttu-id="ed479-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ed479-123">NOTES</span></span>

## <span data-ttu-id="ed479-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ed479-124">RELATED LINKS</span></span>
