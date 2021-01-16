---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagementPartner.dll-Help.xml
Module Name: Az.ManagementPartner
online version: https://docs.microsoft.com/en-us/powershell/module/az.managementpartner/remove-azmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Remove-AzManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Remove-AzManagementPartner.md
ms.openlocfilehash: db87797573d3f6c06b52aa072773c9af1a1be1fb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98428642"
---
# <span data-ttu-id="04a7a-101">Remove-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="04a7a-101">Remove-AzManagementPartner</span></span>

## <span data-ttu-id="04a7a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="04a7a-102">SYNOPSIS</span></span>
<span data-ttu-id="04a7a-103">Exclua a ID da MPN (Microsoft Partner Network) do usuário ou entidade de serviço atual autenticado.</span><span class="sxs-lookup"><span data-stu-id="04a7a-103">Delete the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="04a7a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="04a7a-104">SYNTAX</span></span>

```
Remove-AzManagementPartner [-PartnerId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04a7a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="04a7a-105">DESCRIPTION</span></span>
<span data-ttu-id="04a7a-106">Exclua a ID da MPN (Microsoft Partner Network) do usuário ou entidade de serviço atual autenticado.</span><span class="sxs-lookup"><span data-stu-id="04a7a-106">Delete the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="04a7a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="04a7a-107">EXAMPLES</span></span>

### <span data-ttu-id="04a7a-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="04a7a-108">Example 1</span></span>
```powershell
PS C:\>Remove-AzManagementPartner -PartnerId 123457 -PassThru
true
```

<span data-ttu-id="04a7a-109">Remover parceiro de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="04a7a-109">Remove management partner</span></span>

## <span data-ttu-id="04a7a-110">OS</span><span class="sxs-lookup"><span data-stu-id="04a7a-110">PARAMETERS</span></span>

### <span data-ttu-id="04a7a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04a7a-111">-DefaultProfile</span></span>
<span data-ttu-id="04a7a-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="04a7a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04a7a-113">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="04a7a-113">-PartnerId</span></span>
<span data-ttu-id="04a7a-114">A ID do parceiro de gerenciamento, é um número de 6 dígitos</span><span class="sxs-lookup"><span data-stu-id="04a7a-114">The management partner id, it is a 6 digits number</span></span>

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

### <span data-ttu-id="04a7a-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="04a7a-115">-PassThru</span></span>
<span data-ttu-id="04a7a-116">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="04a7a-116">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="04a7a-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="04a7a-117">-Confirm</span></span>
<span data-ttu-id="04a7a-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="04a7a-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04a7a-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04a7a-119">-WhatIf</span></span>
<span data-ttu-id="04a7a-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="04a7a-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04a7a-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="04a7a-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04a7a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04a7a-122">CommonParameters</span></span>
<span data-ttu-id="04a7a-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04a7a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04a7a-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04a7a-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04a7a-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="04a7a-125">INPUTS</span></span>

### <span data-ttu-id="04a7a-126">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="04a7a-126">None</span></span>

## <span data-ttu-id="04a7a-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="04a7a-127">OUTPUTS</span></span>

### <span data-ttu-id="04a7a-128">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="04a7a-128">System.Boolean</span></span>

## <span data-ttu-id="04a7a-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="04a7a-129">NOTES</span></span>

## <span data-ttu-id="04a7a-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="04a7a-130">RELATED LINKS</span></span>

[<span data-ttu-id="04a7a-131">New-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="04a7a-131">New-AzManagementPartner</span></span>](./New-AzManagementPartner.md)

[<span data-ttu-id="04a7a-132">Get-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="04a7a-132">Get-AzManagementPartner</span></span>](./Get-AzManagementPartner.md)

[<span data-ttu-id="04a7a-133">Update-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="04a7a-133">Update-AzManagementPartner</span></span>](./Update-AzManagementPartner.md)