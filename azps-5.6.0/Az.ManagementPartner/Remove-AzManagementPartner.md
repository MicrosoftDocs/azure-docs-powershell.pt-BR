---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagementPartner.dll-Help.xml
Module Name: Az.ManagementPartner
online version: https://docs.microsoft.com/powershell/module/az.managementpartner/remove-azmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Remove-AzManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Remove-AzManagementPartner.md
ms.openlocfilehash: 7a213cbe8acacebc0f6e513e264432ca2ba08cf3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890247"
---
# <span data-ttu-id="a7ec1-101">Remove-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="a7ec1-101">Remove-AzManagementPartner</span></span>

## <span data-ttu-id="a7ec1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7ec1-102">SYNOPSIS</span></span>
<span data-ttu-id="a7ec1-103">Exclua a ID do Microsoft Partner Network(MPN) do usuário ou entidade de serviço autenticado atual.</span><span class="sxs-lookup"><span data-stu-id="a7ec1-103">Delete the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="a7ec1-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a7ec1-104">SYNTAX</span></span>

```
Remove-AzManagementPartner [-PartnerId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7ec1-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a7ec1-105">DESCRIPTION</span></span>
<span data-ttu-id="a7ec1-106">Exclua a ID do Microsoft Partner Network(MPN) do usuário ou entidade de serviço autenticado atual.</span><span class="sxs-lookup"><span data-stu-id="a7ec1-106">Delete the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="a7ec1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a7ec1-107">EXAMPLES</span></span>

### <span data-ttu-id="a7ec1-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a7ec1-108">Example 1</span></span>
```powershell
PS C:\>Remove-AzManagementPartner -PartnerId 123457 -PassThru
true
```

<span data-ttu-id="a7ec1-109">Remover parceiro de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="a7ec1-109">Remove management partner</span></span>

## <span data-ttu-id="a7ec1-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a7ec1-110">PARAMETERS</span></span>

### <span data-ttu-id="a7ec1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7ec1-111">-DefaultProfile</span></span>
<span data-ttu-id="a7ec1-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a7ec1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7ec1-113">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="a7ec1-113">-PartnerId</span></span>
<span data-ttu-id="a7ec1-114">A ID do parceiro de gerenciamento, é um número de 6 dígitos</span><span class="sxs-lookup"><span data-stu-id="a7ec1-114">The management partner id, it is a 6 digits number</span></span>

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

### <span data-ttu-id="a7ec1-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a7ec1-115">-PassThru</span></span>
<span data-ttu-id="a7ec1-116">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="a7ec1-116">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7ec1-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a7ec1-117">-Confirm</span></span>
<span data-ttu-id="a7ec1-118">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7ec1-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7ec1-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7ec1-119">-WhatIf</span></span>
<span data-ttu-id="a7ec1-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a7ec1-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7ec1-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a7ec1-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7ec1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7ec1-122">CommonParameters</span></span>
<span data-ttu-id="a7ec1-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7ec1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7ec1-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7ec1-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7ec1-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a7ec1-125">INPUTS</span></span>

### <span data-ttu-id="a7ec1-126">Nenhum</span><span class="sxs-lookup"><span data-stu-id="a7ec1-126">None</span></span>

## <span data-ttu-id="a7ec1-127">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a7ec1-127">OUTPUTS</span></span>

### <span data-ttu-id="a7ec1-128">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a7ec1-128">System.Boolean</span></span>

## <span data-ttu-id="a7ec1-129">NOTES</span><span class="sxs-lookup"><span data-stu-id="a7ec1-129">NOTES</span></span>

## <span data-ttu-id="a7ec1-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a7ec1-130">RELATED LINKS</span></span>

[<span data-ttu-id="a7ec1-131">New-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="a7ec1-131">New-AzManagementPartner</span></span>](./New-AzManagementPartner.md)

[<span data-ttu-id="a7ec1-132">Get-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="a7ec1-132">Get-AzManagementPartner</span></span>](./Get-AzManagementPartner.md)

[<span data-ttu-id="a7ec1-133">Update-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="a7ec1-133">Update-AzManagementPartner</span></span>](./Update-AzManagementPartner.md)