---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagementPartner.dll-Help.xml
Module Name: Az.ManagementPartner
online version: https://docs.microsoft.com/en-us/powershell/module/az.managementpartner/remove-azmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Remove-AzManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Remove-AzManagementPartner.md
ms.openlocfilehash: db87797573d3f6c06b52aa072773c9af1a1be1fb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113000"
---
# <span data-ttu-id="3648b-101">Remove-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="3648b-101">Remove-AzManagementPartner</span></span>

## <span data-ttu-id="3648b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3648b-102">SYNOPSIS</span></span>
<span data-ttu-id="3648b-103">Exclua a ID do MPN (Microsoft Partner Network) do usuário autenticado ou entidade de serviço atual.</span><span class="sxs-lookup"><span data-stu-id="3648b-103">Delete the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="3648b-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3648b-104">SYNTAX</span></span>

```
Remove-AzManagementPartner [-PartnerId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3648b-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="3648b-105">DESCRIPTION</span></span>
<span data-ttu-id="3648b-106">Exclua a ID do MPN (Microsoft Partner Network) do usuário autenticado ou entidade de serviço atual.</span><span class="sxs-lookup"><span data-stu-id="3648b-106">Delete the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="3648b-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3648b-107">EXAMPLES</span></span>

### <span data-ttu-id="3648b-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3648b-108">Example 1</span></span>
```powershell
PS C:\>Remove-AzManagementPartner -PartnerId 123457 -PassThru
true
```

<span data-ttu-id="3648b-109">Remover parceiro de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="3648b-109">Remove management partner</span></span>

## <span data-ttu-id="3648b-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3648b-110">PARAMETERS</span></span>

### <span data-ttu-id="3648b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3648b-111">-DefaultProfile</span></span>
<span data-ttu-id="3648b-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3648b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3648b-113">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="3648b-113">-PartnerId</span></span>
<span data-ttu-id="3648b-114">A ID do parceiro de gerenciamento, é um número de 6 dígitos</span><span class="sxs-lookup"><span data-stu-id="3648b-114">The management partner id, it is a 6 digits number</span></span>

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

### <span data-ttu-id="3648b-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3648b-115">-PassThru</span></span>
<span data-ttu-id="3648b-116">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="3648b-116">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="3648b-117">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="3648b-117">-Confirm</span></span>
<span data-ttu-id="3648b-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3648b-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3648b-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3648b-119">-WhatIf</span></span>
<span data-ttu-id="3648b-120">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="3648b-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3648b-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3648b-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3648b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3648b-122">CommonParameters</span></span>
<span data-ttu-id="3648b-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3648b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3648b-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3648b-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3648b-125">Entradas</span><span class="sxs-lookup"><span data-stu-id="3648b-125">INPUTS</span></span>

### <span data-ttu-id="3648b-126">Nenhum</span><span class="sxs-lookup"><span data-stu-id="3648b-126">None</span></span>

## <span data-ttu-id="3648b-127">Saídas</span><span class="sxs-lookup"><span data-stu-id="3648b-127">OUTPUTS</span></span>

### <span data-ttu-id="3648b-128">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3648b-128">System.Boolean</span></span>

## <span data-ttu-id="3648b-129">Notas</span><span class="sxs-lookup"><span data-stu-id="3648b-129">NOTES</span></span>

## <span data-ttu-id="3648b-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3648b-130">RELATED LINKS</span></span>

[<span data-ttu-id="3648b-131">New-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="3648b-131">New-AzManagementPartner</span></span>](./New-AzManagementPartner.md)

[<span data-ttu-id="3648b-132">Get-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="3648b-132">Get-AzManagementPartner</span></span>](./Get-AzManagementPartner.md)

[<span data-ttu-id="3648b-133">Update-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="3648b-133">Update-AzManagementPartner</span></span>](./Update-AzManagementPartner.md)