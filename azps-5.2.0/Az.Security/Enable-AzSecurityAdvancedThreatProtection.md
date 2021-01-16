---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/enable-azsecurityadvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Enable-AzSecurityAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Enable-AzSecurityAdvancedThreatProtection.md
ms.openlocfilehash: 3db63fad33fe49fe7aa001f13759e41e7cd7c856
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98258964"
---
# <span data-ttu-id="11daa-101">Enable-AzSecurityAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="11daa-101">Enable-AzSecurityAdvancedThreatProtection</span></span>

## <span data-ttu-id="11daa-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="11daa-102">SYNOPSIS</span></span>
<span data-ttu-id="11daa-103">Habilita a política avançada de proteção contra ameaças para uma conta de armazenamento/cosmosDB.</span><span class="sxs-lookup"><span data-stu-id="11daa-103">Enables the advanced threat protection policy for a storage / cosmosDB account.</span></span>

## <span data-ttu-id="11daa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="11daa-104">SYNTAX</span></span>

```
Enable-AzSecurityAdvancedThreatProtection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11daa-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="11daa-105">DESCRIPTION</span></span>
<span data-ttu-id="11daa-106">O `Enable-AzSecurityAdvancedThreatProtection` cmdlet habilita a política de proteção contra ameaças para uma conta de armazenamento/cosmosDB.</span><span class="sxs-lookup"><span data-stu-id="11daa-106">The `Enable-AzSecurityAdvancedThreatProtection` cmdlet enables the threat protection policy for a storage / cosmosDB account.</span></span>
<span data-ttu-id="11daa-107">Para usar esse cmdlet, especifique o parâmetro *ResourceId* .</span><span class="sxs-lookup"><span data-stu-id="11daa-107">To use this cmdlet, specify the *ResourceId* parameter.</span></span>

## <span data-ttu-id="11daa-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="11daa-108">EXAMPLES</span></span>

### <span data-ttu-id="11daa-109">Exemplo 1: conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="11daa-109">Example 1: Storage Account</span></span>
```powershell
PS C:\> Enable-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"

IsEnabled Id
--------- --
    True  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"
```

<span data-ttu-id="11daa-110">Esse comando habilita a política avançada de proteção contra ameaças para a ID do recurso `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"` .</span><span class="sxs-lookup"><span data-stu-id="11daa-110">This command enables the advanced threat protection policy for resource id `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"`.</span></span>

### <span data-ttu-id="11daa-111">Exemplo 2: conta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="11daa-111">Example 2: CosmosDB Account</span></span>
```powershell
PS C:\> Enable-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"

IsEnabled Id
--------- --
    True  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"
```

<span data-ttu-id="11daa-112">Esse comando habilita a política avançada de proteção contra ameaças para a ID do recurso ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"` .</span><span class="sxs-lookup"><span data-stu-id="11daa-112">This command enables the advanced threat protection policy for resource id ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"`.</span></span>

## <span data-ttu-id="11daa-113">OS</span><span class="sxs-lookup"><span data-stu-id="11daa-113">PARAMETERS</span></span>

### <span data-ttu-id="11daa-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11daa-114">-DefaultProfile</span></span>
<span data-ttu-id="11daa-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="11daa-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11daa-116">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="11daa-116">-ResourceId</span></span>
<span data-ttu-id="11daa-117">ID do recurso de segurança no qual você deseja invocar o comando.</span><span class="sxs-lookup"><span data-stu-id="11daa-117">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="11daa-118">-Confirme</span><span class="sxs-lookup"><span data-stu-id="11daa-118">-Confirm</span></span>
<span data-ttu-id="11daa-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11daa-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11daa-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11daa-120">-WhatIf</span></span>
<span data-ttu-id="11daa-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="11daa-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="11daa-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="11daa-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11daa-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11daa-123">CommonParameters</span></span>
<span data-ttu-id="11daa-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11daa-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11daa-125">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="11daa-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11daa-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="11daa-126">INPUTS</span></span>

### <span data-ttu-id="11daa-127">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="11daa-127">None</span></span>

## <span data-ttu-id="11daa-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="11daa-128">OUTPUTS</span></span>

### <span data-ttu-id="11daa-129">Microsoft. Azure. Commands. Security. Models. AdvancedThreatProtection. PSAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="11daa-129">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span></span>

## <span data-ttu-id="11daa-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="11daa-130">NOTES</span></span>

## <span data-ttu-id="11daa-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="11daa-131">RELATED LINKS</span></span>
