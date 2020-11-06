---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: 9FD4DB8C-B242-4F9A-92E5-0B3EDED00521
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devtestlabs/get-azurermdtlautostartpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlAutoStartPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlAutoStartPolicy.md
ms.openlocfilehash: efe948e2676b44a70917efb43e901f8848dec0e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429560"
---
# <span data-ttu-id="b40e6-101">Get-AzureRmDtlAutoStartPolicy</span><span class="sxs-lookup"><span data-stu-id="b40e6-101">Get-AzureRmDtlAutoStartPolicy</span></span>

## <span data-ttu-id="b40e6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b40e6-102">SYNOPSIS</span></span>
<span data-ttu-id="b40e6-103">Obtém a política de início automático de um laboratório no DevTest Labs.</span><span class="sxs-lookup"><span data-stu-id="b40e6-103">Gets the auto start policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b40e6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b40e6-104">SYNTAX</span></span>

```
Get-AzureRmDtlAutoStartPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b40e6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b40e6-105">DESCRIPTION</span></span>
<span data-ttu-id="b40e6-106">O cmdlet **Get-AzureRmDtlAutoStartPolicy** Obtém a política de início automático de um laboratório que programa máquinas virtuais de laboratório para início automático.</span><span class="sxs-lookup"><span data-stu-id="b40e6-106">The **Get-AzureRmDtlAutoStartPolicy** cmdlet gets the auto start policy of a lab which schedules lab virtual machines for automatic start.</span></span>
<span data-ttu-id="b40e6-107">O cmdlet retorna o status habilitado ou desabilitado da política e os dias da semana e a hora do dia que você definiu para permitir que as máquinas virtuais de laboratório sejam agendadas para início automático.</span><span class="sxs-lookup"><span data-stu-id="b40e6-107">The cmdlet returns the enabled or disabled status of the policy and the days of the week and time of day that you have set to allow lab virtual machines to be scheduled for automatic start.</span></span>

## <span data-ttu-id="b40e6-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b40e6-108">EXAMPLES</span></span>

## <span data-ttu-id="b40e6-109">OS</span><span class="sxs-lookup"><span data-stu-id="b40e6-109">PARAMETERS</span></span>

### <span data-ttu-id="b40e6-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b40e6-110">-DefaultProfile</span></span>
<span data-ttu-id="b40e6-111">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="b40e6-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b40e6-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="b40e6-112">-LabName</span></span>
<span data-ttu-id="b40e6-113">Especifica o nome do laboratório para o qual esse cmdlet obtém a política de início automático.</span><span class="sxs-lookup"><span data-stu-id="b40e6-113">Specifies the name of the lab for which this cmdlet gets the auto start policy.</span></span>

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

### <span data-ttu-id="b40e6-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b40e6-114">-ResourceGroupName</span></span>
<span data-ttu-id="b40e6-115">Especifica o nome do grupo de recursos ao qual o laboratório pertence.</span><span class="sxs-lookup"><span data-stu-id="b40e6-115">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="b40e6-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b40e6-116">CommonParameters</span></span>
<span data-ttu-id="b40e6-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b40e6-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b40e6-118">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b40e6-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b40e6-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b40e6-119">INPUTS</span></span>

### <span data-ttu-id="b40e6-120">System. String</span><span class="sxs-lookup"><span data-stu-id="b40e6-120">System.String</span></span>

## <span data-ttu-id="b40e6-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b40e6-121">OUTPUTS</span></span>

### <span data-ttu-id="b40e6-122">Microsoft. Azure. Commands. DevTestLabs. Models. PSSchedule</span><span class="sxs-lookup"><span data-stu-id="b40e6-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSSchedule</span></span>

## <span data-ttu-id="b40e6-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b40e6-123">NOTES</span></span>

## <span data-ttu-id="b40e6-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b40e6-124">RELATED LINKS</span></span>

[<span data-ttu-id="b40e6-125">Set-AzureRmDtlAutoStartPolicy</span><span class="sxs-lookup"><span data-stu-id="b40e6-125">Set-AzureRmDtlAutoStartPolicy</span></span>](./Set-AzureRmDtlAutoStartPolicy.md)


