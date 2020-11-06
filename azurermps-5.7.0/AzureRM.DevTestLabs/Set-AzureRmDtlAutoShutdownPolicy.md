---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: 8AAD9309-5763-4903-AF6A-1E50310146C0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devtestlabs/set-azurermdtlautoshutdownpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlAutoShutdownPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlAutoShutdownPolicy.md
ms.openlocfilehash: edded91551b87e180b17ff8f97d84d16bef0b0ce
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440466"
---
# <span data-ttu-id="658e6-101">Set-AzureRmDtlAutoShutdownPolicy</span><span class="sxs-lookup"><span data-stu-id="658e6-101">Set-AzureRmDtlAutoShutdownPolicy</span></span>

## <span data-ttu-id="658e6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="658e6-102">SYNOPSIS</span></span>
<span data-ttu-id="658e6-103">Define a política de desligamento automático de um laboratório DevTest Labs.</span><span class="sxs-lookup"><span data-stu-id="658e6-103">Sets the auto shutdown policy of a lab DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="658e6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="658e6-104">SYNTAX</span></span>

### <span data-ttu-id="658e6-105">Habilitar (padrão)</span><span class="sxs-lookup"><span data-stu-id="658e6-105">Enable (Default)</span></span>
```
Set-AzureRmDtlAutoShutdownPolicy [[-Time] <DateTime>] [-Enable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="658e6-106">Desabilita</span><span class="sxs-lookup"><span data-stu-id="658e6-106">Disable</span></span>
```
Set-AzureRmDtlAutoShutdownPolicy [[-Time] <DateTime>] [-Disable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="658e6-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="658e6-107">DESCRIPTION</span></span>
<span data-ttu-id="658e6-108">O cmdlet **set-AzureRmDtlAutoShutdownPolicy** define a política de desligamento automático de um laboratório, que automaticamente desliga todas as máquinas virtuais do laboratório em um horário especificado do dia.</span><span class="sxs-lookup"><span data-stu-id="658e6-108">The **Set-AzureRmDtlAutoShutdownPolicy** cmdlet sets the auto shutdown policy of a lab, which automatically shuts down all the virtual machines in the lab at a specified time of the day.</span></span>
<span data-ttu-id="658e6-109">O cmdlet usa o grupo de recursos e o nome do laboratório especificado para definir a política.</span><span class="sxs-lookup"><span data-stu-id="658e6-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="658e6-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="658e6-110">EXAMPLES</span></span>

## <span data-ttu-id="658e6-111">OS</span><span class="sxs-lookup"><span data-stu-id="658e6-111">PARAMETERS</span></span>

### <span data-ttu-id="658e6-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="658e6-112">-DefaultProfile</span></span>
<span data-ttu-id="658e6-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="658e6-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="658e6-114">-Disable</span><span class="sxs-lookup"><span data-stu-id="658e6-114">-Disable</span></span>
<span data-ttu-id="658e6-115">Indica que o cmdlet desabilita a política do laboratório.</span><span class="sxs-lookup"><span data-stu-id="658e6-115">Indicates that the cmdlet disables the policy in the lab.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Disable
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="658e6-116">-Habilitar</span><span class="sxs-lookup"><span data-stu-id="658e6-116">-Enable</span></span>
<span data-ttu-id="658e6-117">Indica que o cmdlet habilita a política no laboratório.</span><span class="sxs-lookup"><span data-stu-id="658e6-117">Indicates that the cmdlet enables the policy in the lab.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Enable
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="658e6-118">-LabName</span><span class="sxs-lookup"><span data-stu-id="658e6-118">-LabName</span></span>
<span data-ttu-id="658e6-119">Especifica o nome do laboratório para o qual esse cmdlet define a política de desligamento automático.</span><span class="sxs-lookup"><span data-stu-id="658e6-119">Specifies the name of the lab for which this cmdlet sets the auto shutdown policy.</span></span>

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

### <span data-ttu-id="658e6-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="658e6-120">-ResourceGroupName</span></span>
<span data-ttu-id="658e6-121">Especifica o nome do grupo de recursos ao qual o laboratório pertence.</span><span class="sxs-lookup"><span data-stu-id="658e6-121">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="658e6-122">-Time</span><span class="sxs-lookup"><span data-stu-id="658e6-122">-Time</span></span>
<span data-ttu-id="658e6-123">Especifica o tempo, como um objeto **DateTime** , para quando as máquinas virtuais no laboratório devem desligar.</span><span class="sxs-lookup"><span data-stu-id="658e6-123">Specifies the time, as a **DateTime** object, for when the virtual machines in the lab must shut down.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="658e6-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="658e6-124">-Confirm</span></span>
<span data-ttu-id="658e6-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="658e6-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="658e6-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="658e6-126">-WhatIf</span></span>
<span data-ttu-id="658e6-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="658e6-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="658e6-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="658e6-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="658e6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="658e6-129">CommonParameters</span></span>
<span data-ttu-id="658e6-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="658e6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="658e6-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="658e6-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="658e6-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="658e6-132">INPUTS</span></span>

### <span data-ttu-id="658e6-133">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="658e6-133">None</span></span>
<span data-ttu-id="658e6-134">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="658e6-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="658e6-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="658e6-135">OUTPUTS</span></span>

### <span data-ttu-id="658e6-136">Microsoft. Azure. Commands. DevTestLabs. Models. PSSchedule</span><span class="sxs-lookup"><span data-stu-id="658e6-136">Microsoft.Azure.Commands.DevTestLabs.Models.PSSchedule</span></span>
<span data-ttu-id="658e6-137">Esse cmdlet retorna o cronograma que especifica quando as máquinas virtuais no laboratório devem desligar.</span><span class="sxs-lookup"><span data-stu-id="658e6-137">This cmdlet returns the schedule which specifies when the virtual machines in the lab must shut down.</span></span>

## <span data-ttu-id="658e6-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="658e6-138">NOTES</span></span>

## <span data-ttu-id="658e6-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="658e6-139">RELATED LINKS</span></span>

[<span data-ttu-id="658e6-140">Get-AzureRmDtlAutoShutdownPolicy</span><span class="sxs-lookup"><span data-stu-id="658e6-140">Get-AzureRmDtlAutoShutdownPolicy</span></span>](./Get-AzureRmDtlAutoShutdownPolicy.md)

