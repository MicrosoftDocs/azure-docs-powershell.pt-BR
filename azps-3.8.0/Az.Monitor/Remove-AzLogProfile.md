---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: DDA137FD-4EB3-4FB7-A202-978922038AFC
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzLogProfile.md
ms.openlocfilehash: 3c8dda7d7b84ae4ee7017c88e211b2ab5db46360
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93777277"
---
# <span data-ttu-id="e5de2-101">Remove-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="e5de2-101">Remove-AzLogProfile</span></span>

## <span data-ttu-id="e5de2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e5de2-102">SYNOPSIS</span></span>
<span data-ttu-id="e5de2-103">Remove um perfil de log.</span><span class="sxs-lookup"><span data-stu-id="e5de2-103">Removes a log profile.</span></span>

## <span data-ttu-id="e5de2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e5de2-104">SYNTAX</span></span>

```
Remove-AzLogProfile -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e5de2-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e5de2-105">DESCRIPTION</span></span>
<span data-ttu-id="e5de2-106">O cmdlet **Remove-AzLogProfile** remove um perfil de log.</span><span class="sxs-lookup"><span data-stu-id="e5de2-106">The **Remove-AzLogProfile** cmdlet removes a log profile.</span></span>
<span data-ttu-id="e5de2-107">Esse cmdlet implementa o padrão ShouldProcess, ou seja, ele pode solicitar confirmação do usuário antes de realmente criar, modificar ou remover o recurso.</span><span class="sxs-lookup"><span data-stu-id="e5de2-107">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="e5de2-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e5de2-108">EXAMPLES</span></span>

## <span data-ttu-id="e5de2-109">OS</span><span class="sxs-lookup"><span data-stu-id="e5de2-109">PARAMETERS</span></span>

### <span data-ttu-id="e5de2-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5de2-110">-DefaultProfile</span></span>
<span data-ttu-id="e5de2-111">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="e5de2-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e5de2-112">-Nome</span><span class="sxs-lookup"><span data-stu-id="e5de2-112">-Name</span></span>
<span data-ttu-id="e5de2-113">Especifica o nome do perfil de log a ser removido.</span><span class="sxs-lookup"><span data-stu-id="e5de2-113">Specifies the name of the log profile to remove.</span></span>

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

### <span data-ttu-id="e5de2-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e5de2-114">-PassThru</span></span>
<span data-ttu-id="e5de2-115">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="e5de2-115">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="e5de2-116">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e5de2-116">-Confirm</span></span>
<span data-ttu-id="e5de2-117">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e5de2-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5de2-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5de2-118">-WhatIf</span></span>
<span data-ttu-id="e5de2-119">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e5de2-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e5de2-120">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e5de2-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5de2-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5de2-121">CommonParameters</span></span>
<span data-ttu-id="e5de2-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5de2-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5de2-123">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e5de2-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5de2-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e5de2-124">INPUTS</span></span>

### <span data-ttu-id="e5de2-125">System. String</span><span class="sxs-lookup"><span data-stu-id="e5de2-125">System.String</span></span>

## <span data-ttu-id="e5de2-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e5de2-126">OUTPUTS</span></span>

### <span data-ttu-id="e5de2-127">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="e5de2-127">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="e5de2-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e5de2-128">NOTES</span></span>

## <span data-ttu-id="e5de2-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e5de2-129">RELATED LINKS</span></span>

[<span data-ttu-id="e5de2-130">Add-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="e5de2-130">Add-AzLogProfile</span></span>](./Add-AzLogProfile.md)

[<span data-ttu-id="e5de2-131">Get-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="e5de2-131">Get-AzLogProfile</span></span>](./Get-AzLogProfile.md)


