---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/enable-azsecurityadvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Enable-AzSecurityAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Enable-AzSecurityAdvancedThreatProtection.md
ms.openlocfilehash: deef0be93c3a80c0db9762907eb52cdc51da9ed3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599263"
---
# <span data-ttu-id="648e6-101">Enable-AzSecurityAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="648e6-101">Enable-AzSecurityAdvancedThreatProtection</span></span>

## <span data-ttu-id="648e6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="648e6-102">SYNOPSIS</span></span>
<span data-ttu-id="648e6-103">Habilita a política avançada de proteção contra ameaças para uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="648e6-103">Enables the advanced threat protection policy for a storage account.</span></span>

## <span data-ttu-id="648e6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="648e6-104">SYNTAX</span></span>

```
Enable-AzSecurityAdvancedThreatProtection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="648e6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="648e6-105">DESCRIPTION</span></span>
<span data-ttu-id="648e6-106">O `Enable-AzSecurityAdvancedThreatProtection` cmdlet habilita a política de protetion de ameaças para uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="648e6-106">The `Enable-AzSecurityAdvancedThreatProtection` cmdlet enables the threat protetion policy for a storage account.</span></span>
<span data-ttu-id="648e6-107">Para usar esse cmdlet, especifique o parâmetro *ResourceId* .</span><span class="sxs-lookup"><span data-stu-id="648e6-107">To use this cmdlet, specify the *ResourceId* parameter.</span></span>

## <span data-ttu-id="648e6-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="648e6-108">EXAMPLES</span></span>

### <span data-ttu-id="648e6-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="648e6-109">Example 1</span></span>
```powershell
PS C:\> Enable-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"

IsEnabled Id
--------- --
    True  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"
```

<span data-ttu-id="648e6-110">Esse comando habilita a política avançada de proteção contra ameaças para a ID do recurso `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"` .</span><span class="sxs-lookup"><span data-stu-id="648e6-110">This command enables the advanced threat protection policy for resource id `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"`.</span></span>

## <span data-ttu-id="648e6-111">OS</span><span class="sxs-lookup"><span data-stu-id="648e6-111">PARAMETERS</span></span>

### <span data-ttu-id="648e6-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="648e6-112">-DefaultProfile</span></span>
<span data-ttu-id="648e6-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="648e6-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="648e6-114">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="648e6-114">-ResourceId</span></span>
<span data-ttu-id="648e6-115">ID do recurso de segurança no qual você deseja invocar o comando.</span><span class="sxs-lookup"><span data-stu-id="648e6-115">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="648e6-116">-Confirme</span><span class="sxs-lookup"><span data-stu-id="648e6-116">-Confirm</span></span>
<span data-ttu-id="648e6-117">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="648e6-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="648e6-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="648e6-118">-WhatIf</span></span>
<span data-ttu-id="648e6-119">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="648e6-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="648e6-120">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="648e6-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="648e6-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="648e6-121">CommonParameters</span></span>
<span data-ttu-id="648e6-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="648e6-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="648e6-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="648e6-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="648e6-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="648e6-124">INPUTS</span></span>

### <span data-ttu-id="648e6-125">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="648e6-125">None</span></span>

## <span data-ttu-id="648e6-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="648e6-126">OUTPUTS</span></span>

### <span data-ttu-id="648e6-127">Microsoft. Azure. Commands. Security. Models. AdvancedThreatProtection. PSAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="648e6-127">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span></span>

## <span data-ttu-id="648e6-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="648e6-128">NOTES</span></span>

## <span data-ttu-id="648e6-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="648e6-129">RELATED LINKS</span></span>
