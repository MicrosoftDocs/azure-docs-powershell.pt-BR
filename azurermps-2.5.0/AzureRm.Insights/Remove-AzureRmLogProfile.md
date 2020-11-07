---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: DDA137FD-4EB3-4FB7-A202-978922038AFC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/remove-azurermlogprofile
schema: 2.0.0
ms.openlocfilehash: 78d2bff42382564bb07f680b5db8db39707ffb97
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785244"
---
# <span data-ttu-id="f0c37-101">Remove-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="f0c37-101">Remove-AzureRmLogProfile</span></span>

## <span data-ttu-id="f0c37-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f0c37-102">SYNOPSIS</span></span>
<span data-ttu-id="f0c37-103">Remove um perfil de log.</span><span class="sxs-lookup"><span data-stu-id="f0c37-103">Removes a log profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f0c37-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f0c37-104">SYNTAX</span></span>

```
Remove-AzureRmLogProfile -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0c37-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f0c37-105">DESCRIPTION</span></span>
<span data-ttu-id="f0c37-106">O cmdlet **Remove-AzureRmLogProfile** remove um perfil de log.</span><span class="sxs-lookup"><span data-stu-id="f0c37-106">The **Remove-AzureRmLogProfile** cmdlet removes a log profile.</span></span>
<span data-ttu-id="f0c37-107">Esse cmdlet implementa o padrão ShouldProcess, ou seja, ele pode solicitar confirmação do usuário antes de realmente criar, modificar ou remover o recurso.</span><span class="sxs-lookup"><span data-stu-id="f0c37-107">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="f0c37-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f0c37-108">EXAMPLES</span></span>

## <span data-ttu-id="f0c37-109">OS</span><span class="sxs-lookup"><span data-stu-id="f0c37-109">PARAMETERS</span></span>

### <span data-ttu-id="f0c37-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0c37-110">-DefaultProfile</span></span>
<span data-ttu-id="f0c37-111">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="f0c37-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0c37-112">-Nome</span><span class="sxs-lookup"><span data-stu-id="f0c37-112">-Name</span></span>
<span data-ttu-id="f0c37-113">Especifica o nome do perfil de log a ser removido.</span><span class="sxs-lookup"><span data-stu-id="f0c37-113">Specifies the name of the log profile to remove.</span></span>

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

### <span data-ttu-id="f0c37-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f0c37-114">-PassThru</span></span>
<span data-ttu-id="f0c37-115">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="f0c37-115">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="f0c37-116">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f0c37-116">-Confirm</span></span>
<span data-ttu-id="f0c37-117">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f0c37-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0c37-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0c37-118">-WhatIf</span></span>
<span data-ttu-id="f0c37-119">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f0c37-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f0c37-120">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f0c37-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0c37-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0c37-121">CommonParameters</span></span>
<span data-ttu-id="f0c37-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0c37-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0c37-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0c37-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0c37-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f0c37-124">INPUTS</span></span>

### <span data-ttu-id="f0c37-125">System. String</span><span class="sxs-lookup"><span data-stu-id="f0c37-125">System.String</span></span>

## <span data-ttu-id="f0c37-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f0c37-126">OUTPUTS</span></span>

### <span data-ttu-id="f0c37-127">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="f0c37-127">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="f0c37-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f0c37-128">NOTES</span></span>

## <span data-ttu-id="f0c37-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f0c37-129">RELATED LINKS</span></span>

[<span data-ttu-id="f0c37-130">Add-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="f0c37-130">Add-AzureRmLogProfile</span></span>](./Add-AzureRmLogProfile.md)

[<span data-ttu-id="f0c37-131">Get-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="f0c37-131">Get-AzureRmLogProfile</span></span>](./Get-AzureRmLogProfile.md)


