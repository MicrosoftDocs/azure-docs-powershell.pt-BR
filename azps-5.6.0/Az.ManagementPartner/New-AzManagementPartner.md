---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagementPartner.dll-Help.xml
Module Name: Az.ManagementPartner
online version: https://docs.microsoft.com/powershell/module/az.managementpartner/new-azmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/New-AzManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/New-AzManagementPartner.md
ms.openlocfilehash: 57d9f5d51cb2646274728f8b2f6d846bd954f2a7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890839"
---
# <span data-ttu-id="07678-101">New-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="07678-101">New-AzManagementPartner</span></span>

## <span data-ttu-id="07678-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07678-102">SYNOPSIS</span></span>
<span data-ttu-id="07678-103">Associa uma ID do Microsoft Partner Network (MPN) ao usuário ou entidade de serviço autenticado atual.</span><span class="sxs-lookup"><span data-stu-id="07678-103">Associates a Microsoft Partner Network(MPN) ID to the current authenticated user or service principal.</span></span>

## <span data-ttu-id="07678-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="07678-104">SYNTAX</span></span>

```
New-AzManagementPartner [-PartnerId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="07678-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="07678-105">DESCRIPTION</span></span>
<span data-ttu-id="07678-106">Associa uma ID do Microsoft Partner Network (MPN) ao usuário ou entidade de serviço autenticado atual.</span><span class="sxs-lookup"><span data-stu-id="07678-106">Associates a Microsoft Partner Network(MPN) ID to the current authenticated user or service principal.</span></span>

## <span data-ttu-id="07678-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="07678-107">EXAMPLES</span></span>

### <span data-ttu-id="07678-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="07678-108">Example 1</span></span>
```powershell
PS C:\> New-AzManagementPartner -PartnerId 4977985
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="07678-109">Adicionar um parceiro de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="07678-109">Add a management partner</span></span>

## <span data-ttu-id="07678-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="07678-110">PARAMETERS</span></span>

### <span data-ttu-id="07678-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07678-111">-DefaultProfile</span></span>
<span data-ttu-id="07678-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="07678-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07678-113">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="07678-113">-PartnerId</span></span>
<span data-ttu-id="07678-114">A ID do parceiro de gerenciamento, é um número de 6 dígitos</span><span class="sxs-lookup"><span data-stu-id="07678-114">The management partner id, it is a 6 digits number</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07678-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="07678-115">-Confirm</span></span>
<span data-ttu-id="07678-116">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="07678-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07678-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07678-117">-WhatIf</span></span>
<span data-ttu-id="07678-118">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="07678-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07678-119">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="07678-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07678-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07678-120">CommonParameters</span></span>
<span data-ttu-id="07678-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07678-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07678-122">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07678-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07678-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="07678-123">INPUTS</span></span>

### <span data-ttu-id="07678-124">Nenhum</span><span class="sxs-lookup"><span data-stu-id="07678-124">None</span></span>

## <span data-ttu-id="07678-125">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="07678-125">OUTPUTS</span></span>

### <span data-ttu-id="07678-126">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span><span class="sxs-lookup"><span data-stu-id="07678-126">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span></span>

## <span data-ttu-id="07678-127">NOTES</span><span class="sxs-lookup"><span data-stu-id="07678-127">NOTES</span></span>

## <span data-ttu-id="07678-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="07678-128">RELATED LINKS</span></span>

[<span data-ttu-id="07678-129">Remove-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="07678-129">Remove-AzManagementPartner</span></span>](./Remove-AzManagementPartner.md)

[<span data-ttu-id="07678-130">Get-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="07678-130">Get-AzManagementPartner</span></span>](./Get-AzManagementPartner.md)

[<span data-ttu-id="07678-131">Update-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="07678-131">Update-AzManagementPartner</span></span>](./Update-AzManagementPartner.md)