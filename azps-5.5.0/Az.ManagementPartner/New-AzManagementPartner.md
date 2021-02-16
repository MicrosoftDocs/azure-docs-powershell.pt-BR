---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagementPartner.dll-Help.xml
Module Name: Az.ManagementPartner
online version: https://docs.microsoft.com/en-us/powershell/module/az.managementpartner/new-azmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/New-AzManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/New-AzManagementPartner.md
ms.openlocfilehash: 9e6c56fa48b71e2571b7702e170bdc3e9e41f3aa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117571"
---
# <span data-ttu-id="89202-101">New-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="89202-101">New-AzManagementPartner</span></span>

## <span data-ttu-id="89202-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="89202-102">SYNOPSIS</span></span>
<span data-ttu-id="89202-103">Associa uma ID do Microsoft Partner Network (MPN) ao usuário autenticado ou entidade de serviço atual.</span><span class="sxs-lookup"><span data-stu-id="89202-103">Associates a Microsoft Partner Network(MPN) ID to the current authenticated user or service principal.</span></span>

## <span data-ttu-id="89202-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="89202-104">SYNTAX</span></span>

```
New-AzManagementPartner [-PartnerId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="89202-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="89202-105">DESCRIPTION</span></span>
<span data-ttu-id="89202-106">Associa uma ID do Microsoft Partner Network (MPN) ao usuário autenticado ou entidade de serviço atual.</span><span class="sxs-lookup"><span data-stu-id="89202-106">Associates a Microsoft Partner Network(MPN) ID to the current authenticated user or service principal.</span></span>

## <span data-ttu-id="89202-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="89202-107">EXAMPLES</span></span>

### <span data-ttu-id="89202-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="89202-108">Example 1</span></span>
```powershell
PS C:\> New-AzManagementPartner -PartnerId 4977985
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="89202-109">Adicionar um parceiro de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="89202-109">Add a management partner</span></span>

## <span data-ttu-id="89202-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="89202-110">PARAMETERS</span></span>

### <span data-ttu-id="89202-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89202-111">-DefaultProfile</span></span>
<span data-ttu-id="89202-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="89202-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89202-113">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="89202-113">-PartnerId</span></span>
<span data-ttu-id="89202-114">A ID do parceiro de gerenciamento, é um número de 6 dígitos</span><span class="sxs-lookup"><span data-stu-id="89202-114">The management partner id, it is a 6 digits number</span></span>

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

### <span data-ttu-id="89202-115">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="89202-115">-Confirm</span></span>
<span data-ttu-id="89202-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89202-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89202-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89202-117">-WhatIf</span></span>
<span data-ttu-id="89202-118">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="89202-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89202-119">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="89202-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89202-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89202-120">CommonParameters</span></span>
<span data-ttu-id="89202-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89202-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89202-122">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89202-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89202-123">Entradas</span><span class="sxs-lookup"><span data-stu-id="89202-123">INPUTS</span></span>

### <span data-ttu-id="89202-124">Nenhum</span><span class="sxs-lookup"><span data-stu-id="89202-124">None</span></span>

## <span data-ttu-id="89202-125">Saídas</span><span class="sxs-lookup"><span data-stu-id="89202-125">OUTPUTS</span></span>

### <span data-ttu-id="89202-126">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span><span class="sxs-lookup"><span data-stu-id="89202-126">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span></span>

## <span data-ttu-id="89202-127">Notas</span><span class="sxs-lookup"><span data-stu-id="89202-127">NOTES</span></span>

## <span data-ttu-id="89202-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="89202-128">RELATED LINKS</span></span>

[<span data-ttu-id="89202-129">Remove-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="89202-129">Remove-AzManagementPartner</span></span>](./Remove-AzManagementPartner.md)

[<span data-ttu-id="89202-130">Get-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="89202-130">Get-AzManagementPartner</span></span>](./Get-AzManagementPartner.md)

[<span data-ttu-id="89202-131">Update-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="89202-131">Update-AzManagementPartner</span></span>](./Update-AzManagementPartner.md)