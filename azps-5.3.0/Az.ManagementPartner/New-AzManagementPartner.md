---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagementPartner.dll-Help.xml
Module Name: Az.ManagementPartner
online version: https://docs.microsoft.com/en-us/powershell/module/az.managementpartner/new-azmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/New-AzManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/New-AzManagementPartner.md
ms.openlocfilehash: 9e6c56fa48b71e2571b7702e170bdc3e9e41f3aa
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98428282"
---
# <span data-ttu-id="32b73-101">New-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="32b73-101">New-AzManagementPartner</span></span>

## <span data-ttu-id="32b73-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="32b73-102">SYNOPSIS</span></span>
<span data-ttu-id="32b73-103">Associa uma ID do Microsoft Partner Network (MPN) ao usuário ou entidade de serviço atual autenticado.</span><span class="sxs-lookup"><span data-stu-id="32b73-103">Associates a Microsoft Partner Network(MPN) ID to the current authenticated user or service principal.</span></span>

## <span data-ttu-id="32b73-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="32b73-104">SYNTAX</span></span>

```
New-AzManagementPartner [-PartnerId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="32b73-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="32b73-105">DESCRIPTION</span></span>
<span data-ttu-id="32b73-106">Associa uma ID do Microsoft Partner Network (MPN) ao usuário ou entidade de serviço atual autenticado.</span><span class="sxs-lookup"><span data-stu-id="32b73-106">Associates a Microsoft Partner Network(MPN) ID to the current authenticated user or service principal.</span></span>

## <span data-ttu-id="32b73-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="32b73-107">EXAMPLES</span></span>

### <span data-ttu-id="32b73-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="32b73-108">Example 1</span></span>
```powershell
PS C:\> New-AzManagementPartner -PartnerId 4977985
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="32b73-109">Adicionar um parceiro de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="32b73-109">Add a management partner</span></span>

## <span data-ttu-id="32b73-110">OS</span><span class="sxs-lookup"><span data-stu-id="32b73-110">PARAMETERS</span></span>

### <span data-ttu-id="32b73-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32b73-111">-DefaultProfile</span></span>
<span data-ttu-id="32b73-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="32b73-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32b73-113">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="32b73-113">-PartnerId</span></span>
<span data-ttu-id="32b73-114">A ID do parceiro de gerenciamento, é um número de 6 dígitos</span><span class="sxs-lookup"><span data-stu-id="32b73-114">The management partner id, it is a 6 digits number</span></span>

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

### <span data-ttu-id="32b73-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="32b73-115">-Confirm</span></span>
<span data-ttu-id="32b73-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="32b73-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32b73-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32b73-117">-WhatIf</span></span>
<span data-ttu-id="32b73-118">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="32b73-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32b73-119">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="32b73-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32b73-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32b73-120">CommonParameters</span></span>
<span data-ttu-id="32b73-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32b73-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32b73-122">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32b73-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32b73-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="32b73-123">INPUTS</span></span>

### <span data-ttu-id="32b73-124">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="32b73-124">None</span></span>

## <span data-ttu-id="32b73-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="32b73-125">OUTPUTS</span></span>

### <span data-ttu-id="32b73-126">Microsoft. Azure. Commands. ManagementPartner. PSManagementPartner</span><span class="sxs-lookup"><span data-stu-id="32b73-126">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span></span>

## <span data-ttu-id="32b73-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="32b73-127">NOTES</span></span>

## <span data-ttu-id="32b73-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="32b73-128">RELATED LINKS</span></span>

[<span data-ttu-id="32b73-129">Remove-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="32b73-129">Remove-AzManagementPartner</span></span>](./Remove-AzManagementPartner.md)

[<span data-ttu-id="32b73-130">Get-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="32b73-130">Get-AzManagementPartner</span></span>](./Get-AzManagementPartner.md)

[<span data-ttu-id="32b73-131">Update-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="32b73-131">Update-AzManagementPartner</span></span>](./Update-AzManagementPartner.md)