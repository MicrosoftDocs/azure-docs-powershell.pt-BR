---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: DDA137FD-4EB3-4FB7-A202-978922038AFC
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzLogProfile.md
ms.openlocfilehash: 008c2b669ffdef61bb0745522f3a5d31775a99d9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772159"
---
# <span data-ttu-id="80d24-101">Remove-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="80d24-101">Remove-AzLogProfile</span></span>

## <span data-ttu-id="80d24-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="80d24-102">SYNOPSIS</span></span>
<span data-ttu-id="80d24-103">Remove um perfil de log.</span><span class="sxs-lookup"><span data-stu-id="80d24-103">Removes a log profile.</span></span>

## <span data-ttu-id="80d24-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="80d24-104">SYNTAX</span></span>

```
Remove-AzLogProfile -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="80d24-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="80d24-105">DESCRIPTION</span></span>
<span data-ttu-id="80d24-106">O cmdlet **Remove-AzLogProfile** remove um perfil de log.</span><span class="sxs-lookup"><span data-stu-id="80d24-106">The **Remove-AzLogProfile** cmdlet removes a log profile.</span></span>
<span data-ttu-id="80d24-107">Esse cmdlet implementa o padrão ShouldProcess, ou seja, ele pode solicitar confirmação do usuário antes de realmente criar, modificar ou remover o recurso.</span><span class="sxs-lookup"><span data-stu-id="80d24-107">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="80d24-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="80d24-108">EXAMPLES</span></span>

## <span data-ttu-id="80d24-109">OS</span><span class="sxs-lookup"><span data-stu-id="80d24-109">PARAMETERS</span></span>

### <span data-ttu-id="80d24-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80d24-110">-DefaultProfile</span></span>
<span data-ttu-id="80d24-111">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="80d24-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="80d24-112">-Nome</span><span class="sxs-lookup"><span data-stu-id="80d24-112">-Name</span></span>
<span data-ttu-id="80d24-113">Especifica o nome do perfil de log a ser removido.</span><span class="sxs-lookup"><span data-stu-id="80d24-113">Specifies the name of the log profile to remove.</span></span>

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

### <span data-ttu-id="80d24-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="80d24-114">-PassThru</span></span>
<span data-ttu-id="80d24-115">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="80d24-115">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="80d24-116">-Confirme</span><span class="sxs-lookup"><span data-stu-id="80d24-116">-Confirm</span></span>
<span data-ttu-id="80d24-117">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="80d24-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80d24-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80d24-118">-WhatIf</span></span>
<span data-ttu-id="80d24-119">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="80d24-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="80d24-120">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="80d24-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80d24-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80d24-121">CommonParameters</span></span>
<span data-ttu-id="80d24-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80d24-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80d24-123">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="80d24-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80d24-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="80d24-124">INPUTS</span></span>

### <span data-ttu-id="80d24-125">System. String</span><span class="sxs-lookup"><span data-stu-id="80d24-125">System.String</span></span>

## <span data-ttu-id="80d24-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="80d24-126">OUTPUTS</span></span>

### <span data-ttu-id="80d24-127">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="80d24-127">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="80d24-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="80d24-128">NOTES</span></span>

## <span data-ttu-id="80d24-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="80d24-129">RELATED LINKS</span></span>

[<span data-ttu-id="80d24-130">Add-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="80d24-130">Add-AzLogProfile</span></span>](./Add-AzLogProfile.md)

[<span data-ttu-id="80d24-131">Get-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="80d24-131">Get-AzLogProfile</span></span>](./Get-AzLogProfile.md)


