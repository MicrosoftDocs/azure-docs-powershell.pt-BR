---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: 9FD4DB8C-B242-4F9A-92E5-0B3EDED00521
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/get-azdtlautostartpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlAutoStartPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlAutoStartPolicy.md
ms.openlocfilehash: 449206713291499c344975e490c3b0d89ab1d88a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93596614"
---
# <span data-ttu-id="d477f-101">Get-AzDtlAutoStartPolicy</span><span class="sxs-lookup"><span data-stu-id="d477f-101">Get-AzDtlAutoStartPolicy</span></span>

## <span data-ttu-id="d477f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d477f-102">SYNOPSIS</span></span>
<span data-ttu-id="d477f-103">Obtém a política de início automático de um laboratório no DevTest Labs.</span><span class="sxs-lookup"><span data-stu-id="d477f-103">Gets the auto start policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="d477f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d477f-104">SYNTAX</span></span>

```
Get-AzDtlAutoStartPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d477f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d477f-105">DESCRIPTION</span></span>
<span data-ttu-id="d477f-106">O cmdlet **Get-AzDtlAutoStartPolicy** Obtém a política de início automático de um laboratório que programa máquinas virtuais de laboratório para início automático.</span><span class="sxs-lookup"><span data-stu-id="d477f-106">The **Get-AzDtlAutoStartPolicy** cmdlet gets the auto start policy of a lab which schedules lab virtual machines for automatic start.</span></span>
<span data-ttu-id="d477f-107">O cmdlet retorna o status habilitado ou desabilitado da política e os dias da semana e a hora do dia que você definiu para permitir que as máquinas virtuais de laboratório sejam agendadas para início automático.</span><span class="sxs-lookup"><span data-stu-id="d477f-107">The cmdlet returns the enabled or disabled status of the policy and the days of the week and time of day that you have set to allow lab virtual machines to be scheduled for automatic start.</span></span>

## <span data-ttu-id="d477f-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d477f-108">EXAMPLES</span></span>

## <span data-ttu-id="d477f-109">OS</span><span class="sxs-lookup"><span data-stu-id="d477f-109">PARAMETERS</span></span>

### <span data-ttu-id="d477f-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d477f-110">-DefaultProfile</span></span>
<span data-ttu-id="d477f-111">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="d477f-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d477f-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="d477f-112">-LabName</span></span>
<span data-ttu-id="d477f-113">Especifica o nome do laboratório para o qual esse cmdlet obtém a política de início automático.</span><span class="sxs-lookup"><span data-stu-id="d477f-113">Specifies the name of the lab for which this cmdlet gets the auto start policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d477f-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d477f-114">-ResourceGroupName</span></span>
<span data-ttu-id="d477f-115">Especifica o nome do grupo de recursos ao qual o laboratório pertence.</span><span class="sxs-lookup"><span data-stu-id="d477f-115">Specifies the name of the resource group that the lab belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d477f-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d477f-116">CommonParameters</span></span>
<span data-ttu-id="d477f-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d477f-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d477f-118">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d477f-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d477f-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d477f-119">INPUTS</span></span>

### <span data-ttu-id="d477f-120">System. String</span><span class="sxs-lookup"><span data-stu-id="d477f-120">System.String</span></span>

## <span data-ttu-id="d477f-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d477f-121">OUTPUTS</span></span>

### <span data-ttu-id="d477f-122">Microsoft. Azure. Commands. DevTestLabs. Models. PSSchedule</span><span class="sxs-lookup"><span data-stu-id="d477f-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSSchedule</span></span>

## <span data-ttu-id="d477f-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d477f-123">NOTES</span></span>

## <span data-ttu-id="d477f-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d477f-124">RELATED LINKS</span></span>

[<span data-ttu-id="d477f-125">Set-AzDtlAutoStartPolicy</span><span class="sxs-lookup"><span data-stu-id="d477f-125">Set-AzDtlAutoStartPolicy</span></span>](./Set-AzDtlAutoStartPolicy.md)


