---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: 5029179A-99A5-4350-A8E5-D15ABA59CC93
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/get-azdtlvmsperuserpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlVMsPerUserPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlVMsPerUserPolicy.md
ms.openlocfilehash: f2d8604de126dcdfa830bdd6650cf66a6db391b5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98429408"
---
# <span data-ttu-id="c8e07-101">Get-AzDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="c8e07-101">Get-AzDtlVMsPerUserPolicy</span></span>

## <span data-ttu-id="c8e07-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c8e07-102">SYNOPSIS</span></span>
<span data-ttu-id="c8e07-103">Obtém a política de máquinas virtuais por usuário de um laboratório no DevTest Labs.</span><span class="sxs-lookup"><span data-stu-id="c8e07-103">Gets the virtual machines per user policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="c8e07-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c8e07-104">SYNTAX</span></span>

```
Get-AzDtlVMsPerUserPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c8e07-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c8e07-105">DESCRIPTION</span></span>
<span data-ttu-id="c8e07-106">O cmdlet **Get-AzDtlVMsPerUserPolicy** Obtém a política de máquinas virtuais por usuário de um laboratório, que permite definir o número máximo de máquinas virtuais permitidas por usuário.</span><span class="sxs-lookup"><span data-stu-id="c8e07-106">The **Get-AzDtlVMsPerUserPolicy** cmdlet gets the virtual machines per user policy of a lab, which allows you to set the maximum number of virtual machines allowed per user.</span></span>
<span data-ttu-id="c8e07-107">O cmdlet retorna o status habilitado ou desabilitado da política e o número máximo de máquinas virtuais permitidas por usuário que você definiu na política.</span><span class="sxs-lookup"><span data-stu-id="c8e07-107">The cmdlet returns the enabled or disabled status of the policy and the maximum number of virtual machines allowed per user that you have set in the policy.</span></span>

## <span data-ttu-id="c8e07-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c8e07-108">EXAMPLES</span></span>

## <span data-ttu-id="c8e07-109">OS</span><span class="sxs-lookup"><span data-stu-id="c8e07-109">PARAMETERS</span></span>

### <span data-ttu-id="c8e07-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8e07-110">-DefaultProfile</span></span>
<span data-ttu-id="c8e07-111">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="c8e07-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c8e07-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="c8e07-112">-LabName</span></span>
<span data-ttu-id="c8e07-113">Especifica o nome do laboratório para o qual esse cmdlet obtém a política por usuário da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c8e07-113">Specifies the name of the lab for which this cmdlet gets the virtual machine per user policy.</span></span>

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

### <span data-ttu-id="c8e07-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8e07-114">-ResourceGroupName</span></span>
<span data-ttu-id="c8e07-115">Especifica o nome do grupo de recursos ao qual o laboratório pertence.</span><span class="sxs-lookup"><span data-stu-id="c8e07-115">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="c8e07-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8e07-116">CommonParameters</span></span>
<span data-ttu-id="c8e07-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8e07-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8e07-118">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8e07-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8e07-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c8e07-119">INPUTS</span></span>

### <span data-ttu-id="c8e07-120">System. String</span><span class="sxs-lookup"><span data-stu-id="c8e07-120">System.String</span></span>

## <span data-ttu-id="c8e07-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c8e07-121">OUTPUTS</span></span>

### <span data-ttu-id="c8e07-122">Microsoft. Azure. Commands. DevTestLabs. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="c8e07-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="c8e07-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c8e07-123">NOTES</span></span>

## <span data-ttu-id="c8e07-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c8e07-124">RELATED LINKS</span></span>

[<span data-ttu-id="c8e07-125">Set-AzDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="c8e07-125">Set-AzDtlVMsPerUserPolicy</span></span>](./Set-AzDtlVMsPerUserPolicy.md)


