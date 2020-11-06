---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: 52DD0511-915F-4144-B47F-E4B7AF403AA5
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/get-azdtlautoshutdownpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlAutoShutdownPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlAutoShutdownPolicy.md
ms.openlocfilehash: 3b34a60fa2b85f18a5bee10e0e1f66a4ab102c7e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93596617"
---
# <span data-ttu-id="c3999-101">Get-AzDtlAutoShutdownPolicy</span><span class="sxs-lookup"><span data-stu-id="c3999-101">Get-AzDtlAutoShutdownPolicy</span></span>

## <span data-ttu-id="c3999-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c3999-102">SYNOPSIS</span></span>
<span data-ttu-id="c3999-103">Obtém a política de desligamento automático de um laboratório no DevTest Labs.</span><span class="sxs-lookup"><span data-stu-id="c3999-103">Gets the auto shutdown policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="c3999-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c3999-104">SYNTAX</span></span>

```
Get-AzDtlAutoShutdownPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c3999-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c3999-105">DESCRIPTION</span></span>
<span data-ttu-id="c3999-106">O cmdlet **Get-AzDtlAutoShutdownPolicy** Obtém a política de desligamento automático de um laboratório, que permite que você desligue automaticamente todas as máquinas virtuais em um laboratório em um horário especificado do dia.</span><span class="sxs-lookup"><span data-stu-id="c3999-106">The **Get-AzDtlAutoShutdownPolicy** cmdlet gets the auto shutdown policy of a lab, which allows you to automatically shut down all the virtual machines in a lab at a specified time of the day.</span></span>
<span data-ttu-id="c3999-107">O cmdlet retorna se o status da política está habilitado e a hora do dia que você definiu para desligar automaticamente as máquinas virtuais de laboratório.</span><span class="sxs-lookup"><span data-stu-id="c3999-107">The cmdlet returns whether the status of the policy is enabled, and the time of day that you have set to automatically shut down the lab virtual machines.</span></span>

## <span data-ttu-id="c3999-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c3999-108">EXAMPLES</span></span>

## <span data-ttu-id="c3999-109">OS</span><span class="sxs-lookup"><span data-stu-id="c3999-109">PARAMETERS</span></span>

### <span data-ttu-id="c3999-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3999-110">-DefaultProfile</span></span>
<span data-ttu-id="c3999-111">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="c3999-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c3999-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="c3999-112">-LabName</span></span>
<span data-ttu-id="c3999-113">Especifica o nome do laboratório para o qual esse cmdlet obtém a política de desligamento automático.</span><span class="sxs-lookup"><span data-stu-id="c3999-113">Specifies the name of the lab for which this cmdlet gets the auto shutdown policy.</span></span>

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

### <span data-ttu-id="c3999-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3999-114">-ResourceGroupName</span></span>
<span data-ttu-id="c3999-115">Especifica o nome do grupo de recursos ao qual o laboratório pertence.</span><span class="sxs-lookup"><span data-stu-id="c3999-115">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="c3999-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3999-116">CommonParameters</span></span>
<span data-ttu-id="c3999-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3999-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3999-118">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3999-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3999-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c3999-119">INPUTS</span></span>

### <span data-ttu-id="c3999-120">System. String</span><span class="sxs-lookup"><span data-stu-id="c3999-120">System.String</span></span>

## <span data-ttu-id="c3999-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c3999-121">OUTPUTS</span></span>

### <span data-ttu-id="c3999-122">Microsoft. Azure. Commands. DevTestLabs. Models. PSSchedule</span><span class="sxs-lookup"><span data-stu-id="c3999-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSSchedule</span></span>

## <span data-ttu-id="c3999-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c3999-123">NOTES</span></span>

## <span data-ttu-id="c3999-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c3999-124">RELATED LINKS</span></span>

[<span data-ttu-id="c3999-125">Set-AzDtlAutoShutdownPolicy</span><span class="sxs-lookup"><span data-stu-id="c3999-125">Set-AzDtlAutoShutdownPolicy</span></span>](./Set-AzDtlAutoShutdownPolicy.md)


