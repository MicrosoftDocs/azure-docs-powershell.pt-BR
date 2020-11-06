---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: 52DD0511-915F-4144-B47F-E4B7AF403AA5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devtestlabs/get-azurermdtlautoshutdownpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlAutoShutdownPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlAutoShutdownPolicy.md
ms.openlocfilehash: 557cfcaefef1a85fe7ad0a8bd62f4ddbf0ecb6f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428932"
---
# <span data-ttu-id="a8589-101">Get-AzureRmDtlAutoShutdownPolicy</span><span class="sxs-lookup"><span data-stu-id="a8589-101">Get-AzureRmDtlAutoShutdownPolicy</span></span>

## <span data-ttu-id="a8589-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a8589-102">SYNOPSIS</span></span>
<span data-ttu-id="a8589-103">Obtém a política de desligamento automático de um laboratório no DevTest Labs.</span><span class="sxs-lookup"><span data-stu-id="a8589-103">Gets the auto shutdown policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a8589-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a8589-104">SYNTAX</span></span>

```
Get-AzureRmDtlAutoShutdownPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a8589-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a8589-105">DESCRIPTION</span></span>
<span data-ttu-id="a8589-106">O cmdlet **Get-AzureRmDtlAutoShutdownPolicy** Obtém a política de desligamento automático de um laboratório, que permite que você desligue automaticamente todas as máquinas virtuais em um laboratório em um horário especificado do dia.</span><span class="sxs-lookup"><span data-stu-id="a8589-106">The **Get-AzureRmDtlAutoShutdownPolicy** cmdlet gets the auto shutdown policy of a lab, which allows you to automatically shut down all the virtual machines in a lab at a specified time of the day.</span></span>
<span data-ttu-id="a8589-107">O cmdlet retorna se o status da política está habilitado e a hora do dia que você definiu para desligar automaticamente as máquinas virtuais de laboratório.</span><span class="sxs-lookup"><span data-stu-id="a8589-107">The cmdlet returns whether the status of the policy is enabled, and the time of day that you have set to automatically shut down the lab virtual machines.</span></span>

## <span data-ttu-id="a8589-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a8589-108">EXAMPLES</span></span>

## <span data-ttu-id="a8589-109">OS</span><span class="sxs-lookup"><span data-stu-id="a8589-109">PARAMETERS</span></span>

### <span data-ttu-id="a8589-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8589-110">-DefaultProfile</span></span>
<span data-ttu-id="a8589-111">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="a8589-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8589-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="a8589-112">-LabName</span></span>
<span data-ttu-id="a8589-113">Especifica o nome do laboratório para o qual esse cmdlet obtém a política de desligamento automático.</span><span class="sxs-lookup"><span data-stu-id="a8589-113">Specifies the name of the lab for which this cmdlet gets the auto shutdown policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8589-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8589-114">-ResourceGroupName</span></span>
<span data-ttu-id="a8589-115">Especifica o nome do grupo de recursos ao qual o laboratório pertence.</span><span class="sxs-lookup"><span data-stu-id="a8589-115">Specifies the name of the resource group that the lab belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8589-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8589-116">CommonParameters</span></span>
<span data-ttu-id="a8589-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8589-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8589-118">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8589-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8589-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a8589-119">INPUTS</span></span>

### <span data-ttu-id="a8589-120">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="a8589-120">None</span></span>
<span data-ttu-id="a8589-121">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="a8589-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a8589-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a8589-122">OUTPUTS</span></span>

### <span data-ttu-id="a8589-123">Microsoft. Azure. Commands. DevTestLabs. Models. PSSchedule</span><span class="sxs-lookup"><span data-stu-id="a8589-123">Microsoft.Azure.Commands.DevTestLabs.Models.PSSchedule</span></span>
<span data-ttu-id="a8589-124">Esse cmdlet retorna o cronograma que especifica quando as máquinas virtuais do laboratório devem desligar.</span><span class="sxs-lookup"><span data-stu-id="a8589-124">This cmdlet returns the schedule which specifies when the lab's virtual machines must shut down.</span></span>

## <span data-ttu-id="a8589-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a8589-125">NOTES</span></span>

## <span data-ttu-id="a8589-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a8589-126">RELATED LINKS</span></span>

[<span data-ttu-id="a8589-127">Set-AzureRmDtlAutoShutdownPolicy</span><span class="sxs-lookup"><span data-stu-id="a8589-127">Set-AzureRmDtlAutoShutdownPolicy</span></span>](./Set-AzureRmDtlAutoShutdownPolicy.md)


