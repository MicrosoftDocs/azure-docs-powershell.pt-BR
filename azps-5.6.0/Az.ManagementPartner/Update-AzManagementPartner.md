---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagementPartner.dll-Help.xml
Module Name: Az.ManagementPartner
online version: https://docs.microsoft.com/powershell/module/az.managementpartner/update-azmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Update-AzManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Update-AzManagementPartner.md
ms.openlocfilehash: 493f4b3e1cfaa3be59d0bd402e2c0d13dfdfad4f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892488"
---
# <span data-ttu-id="23ce0-101">Update-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="23ce0-101">Update-AzManagementPartner</span></span>

## <span data-ttu-id="23ce0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23ce0-102">SYNOPSIS</span></span>
<span data-ttu-id="23ce0-103">Atualiza a ID do Microsoft Partner Network(MPN) do usuário ou entidade de serviço autenticado atual.</span><span class="sxs-lookup"><span data-stu-id="23ce0-103">Updates the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="23ce0-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="23ce0-104">SYNTAX</span></span>

```
Update-AzManagementPartner [-PartnerId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23ce0-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="23ce0-105">DESCRIPTION</span></span>
<span data-ttu-id="23ce0-106">Atualiza a ID do Microsoft Partner Network(MPN) do usuário ou entidade de serviço autenticado atual.</span><span class="sxs-lookup"><span data-stu-id="23ce0-106">Updates the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="23ce0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="23ce0-107">EXAMPLES</span></span>

### <span data-ttu-id="23ce0-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="23ce0-108">Example 1</span></span>
```powershell
PS C:\> Update-AzManagementPartner -PartnerId 4977985
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="23ce0-109">Atualizar o parceiro de gerenciamento para um novo</span><span class="sxs-lookup"><span data-stu-id="23ce0-109">Update the management partner to a new one</span></span>

## <span data-ttu-id="23ce0-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="23ce0-110">PARAMETERS</span></span>

### <span data-ttu-id="23ce0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23ce0-111">-DefaultProfile</span></span>
<span data-ttu-id="23ce0-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="23ce0-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23ce0-113">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="23ce0-113">-PartnerId</span></span>
<span data-ttu-id="23ce0-114">A ID do parceiro de gerenciamento, é um número de 6 dígitos</span><span class="sxs-lookup"><span data-stu-id="23ce0-114">The management partner id, it is a 6 digits number</span></span>

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

### <span data-ttu-id="23ce0-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="23ce0-115">-Confirm</span></span>
<span data-ttu-id="23ce0-116">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23ce0-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23ce0-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23ce0-117">-WhatIf</span></span>
<span data-ttu-id="23ce0-118">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="23ce0-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23ce0-119">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="23ce0-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23ce0-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23ce0-120">CommonParameters</span></span>
<span data-ttu-id="23ce0-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23ce0-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23ce0-122">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23ce0-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23ce0-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="23ce0-123">INPUTS</span></span>

### <span data-ttu-id="23ce0-124">Nenhum</span><span class="sxs-lookup"><span data-stu-id="23ce0-124">None</span></span>

## <span data-ttu-id="23ce0-125">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="23ce0-125">OUTPUTS</span></span>

### <span data-ttu-id="23ce0-126">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span><span class="sxs-lookup"><span data-stu-id="23ce0-126">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span></span>

## <span data-ttu-id="23ce0-127">NOTES</span><span class="sxs-lookup"><span data-stu-id="23ce0-127">NOTES</span></span>

## <span data-ttu-id="23ce0-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="23ce0-128">RELATED LINKS</span></span>

[<span data-ttu-id="23ce0-129">Remove-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="23ce0-129">Remove-AzManagementPartner</span></span>](./Remove-AzManagementPartner.md)

[<span data-ttu-id="23ce0-130">New-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="23ce0-130">New-AzManagementPartner</span></span>](./New-AzManagementPartner.md)

[<span data-ttu-id="23ce0-131">Get-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="23ce0-131">Get-AzManagementPartner</span></span>](./Get-AzManagementPartner.md)