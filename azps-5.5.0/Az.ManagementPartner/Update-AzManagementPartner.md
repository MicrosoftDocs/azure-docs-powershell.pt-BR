---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagementPartner.dll-Help.xml
Module Name: Az.ManagementPartner
online version: https://docs.microsoft.com/en-us/powershell/module/az.managementpartner/update-azmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Update-AzManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Update-AzManagementPartner.md
ms.openlocfilehash: 326e16ff2f5bca8ca5ae987ebedf12cace87e11d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111788"
---
# <span data-ttu-id="01df5-101">Update-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="01df5-101">Update-AzManagementPartner</span></span>

## <span data-ttu-id="01df5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="01df5-102">SYNOPSIS</span></span>
<span data-ttu-id="01df5-103">Atualiza a ID do MPN (Microsoft Partner Network) do usuário ou entidade de serviço autenticado atual.</span><span class="sxs-lookup"><span data-stu-id="01df5-103">Updates the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="01df5-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="01df5-104">SYNTAX</span></span>

```
Update-AzManagementPartner [-PartnerId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01df5-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="01df5-105">DESCRIPTION</span></span>
<span data-ttu-id="01df5-106">Atualiza a ID do MPN (Microsoft Partner Network) do usuário ou entidade de serviço autenticado atual.</span><span class="sxs-lookup"><span data-stu-id="01df5-106">Updates the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="01df5-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="01df5-107">EXAMPLES</span></span>

### <span data-ttu-id="01df5-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="01df5-108">Example 1</span></span>
```powershell
PS C:\> Update-AzManagementPartner -PartnerId 4977985
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="01df5-109">Atualizar o parceiro de gerenciamento para um novo</span><span class="sxs-lookup"><span data-stu-id="01df5-109">Update the management partner to a new one</span></span>

## <span data-ttu-id="01df5-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="01df5-110">PARAMETERS</span></span>

### <span data-ttu-id="01df5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01df5-111">-DefaultProfile</span></span>
<span data-ttu-id="01df5-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="01df5-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01df5-113">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="01df5-113">-PartnerId</span></span>
<span data-ttu-id="01df5-114">A ID do parceiro de gerenciamento, é um número de 6 dígitos</span><span class="sxs-lookup"><span data-stu-id="01df5-114">The management partner id, it is a 6 digits number</span></span>

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

### <span data-ttu-id="01df5-115">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="01df5-115">-Confirm</span></span>
<span data-ttu-id="01df5-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="01df5-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01df5-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01df5-117">-WhatIf</span></span>
<span data-ttu-id="01df5-118">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="01df5-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01df5-119">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="01df5-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01df5-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01df5-120">CommonParameters</span></span>
<span data-ttu-id="01df5-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01df5-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01df5-122">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01df5-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01df5-123">Entradas</span><span class="sxs-lookup"><span data-stu-id="01df5-123">INPUTS</span></span>

### <span data-ttu-id="01df5-124">Nenhum</span><span class="sxs-lookup"><span data-stu-id="01df5-124">None</span></span>

## <span data-ttu-id="01df5-125">Saídas</span><span class="sxs-lookup"><span data-stu-id="01df5-125">OUTPUTS</span></span>

### <span data-ttu-id="01df5-126">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span><span class="sxs-lookup"><span data-stu-id="01df5-126">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span></span>

## <span data-ttu-id="01df5-127">Notas</span><span class="sxs-lookup"><span data-stu-id="01df5-127">NOTES</span></span>

## <span data-ttu-id="01df5-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="01df5-128">RELATED LINKS</span></span>

[<span data-ttu-id="01df5-129">Remove-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="01df5-129">Remove-AzManagementPartner</span></span>](./Remove-AzManagementPartner.md)

[<span data-ttu-id="01df5-130">New-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="01df5-130">New-AzManagementPartner</span></span>](./New-AzManagementPartner.md)

[<span data-ttu-id="01df5-131">Get-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="01df5-131">Get-AzManagementPartner</span></span>](./Get-AzManagementPartner.md)