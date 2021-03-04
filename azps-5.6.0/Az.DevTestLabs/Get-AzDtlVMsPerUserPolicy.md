---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: 5029179A-99A5-4350-A8E5-D15ABA59CC93
online version: https://docs.microsoft.com/powershell/module/az.devtestlabs/get-azdtlvmsperuserpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlVMsPerUserPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlVMsPerUserPolicy.md
ms.openlocfilehash: 7c2a7ef4c134d811d8c30266305f25d3d53b1289
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892177"
---
# <span data-ttu-id="fcc07-101">Get-AzDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="fcc07-101">Get-AzDtlVMsPerUserPolicy</span></span>

## <span data-ttu-id="fcc07-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fcc07-102">SYNOPSIS</span></span>
<span data-ttu-id="fcc07-103">Obtém as máquinas virtuais por política de usuário de um laboratório em DevTest Labs.</span><span class="sxs-lookup"><span data-stu-id="fcc07-103">Gets the virtual machines per user policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="fcc07-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="fcc07-104">SYNTAX</span></span>

```
Get-AzDtlVMsPerUserPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fcc07-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="fcc07-105">DESCRIPTION</span></span>
<span data-ttu-id="fcc07-106">O cmdlet **Get-AzDtlVMsPerUserPolicy** obtém as máquinas virtuais por política de usuário de um laboratório, o que permite definir o número máximo de máquinas virtuais permitidas por usuário.</span><span class="sxs-lookup"><span data-stu-id="fcc07-106">The **Get-AzDtlVMsPerUserPolicy** cmdlet gets the virtual machines per user policy of a lab, which allows you to set the maximum number of virtual machines allowed per user.</span></span>
<span data-ttu-id="fcc07-107">O cmdlet retorna o status habilitado ou desabilitado da política e o número máximo de máquinas virtuais permitidas por usuário que você definiu na política.</span><span class="sxs-lookup"><span data-stu-id="fcc07-107">The cmdlet returns the enabled or disabled status of the policy and the maximum number of virtual machines allowed per user that you have set in the policy.</span></span>

## <span data-ttu-id="fcc07-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fcc07-108">EXAMPLES</span></span>

## <span data-ttu-id="fcc07-109">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="fcc07-109">PARAMETERS</span></span>

### <span data-ttu-id="fcc07-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcc07-110">-DefaultProfile</span></span>
<span data-ttu-id="fcc07-111">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="fcc07-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fcc07-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="fcc07-112">-LabName</span></span>
<span data-ttu-id="fcc07-113">Especifica o nome do laboratório para o qual esse cmdlet obtém a máquina virtual por política de usuário.</span><span class="sxs-lookup"><span data-stu-id="fcc07-113">Specifies the name of the lab for which this cmdlet gets the virtual machine per user policy.</span></span>

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

### <span data-ttu-id="fcc07-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fcc07-114">-ResourceGroupName</span></span>
<span data-ttu-id="fcc07-115">Especifica o nome do grupo de recursos ao que o laboratório pertence.</span><span class="sxs-lookup"><span data-stu-id="fcc07-115">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="fcc07-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcc07-116">CommonParameters</span></span>
<span data-ttu-id="fcc07-117">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fcc07-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcc07-118">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fcc07-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcc07-119">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fcc07-119">INPUTS</span></span>

### <span data-ttu-id="fcc07-120">System.String</span><span class="sxs-lookup"><span data-stu-id="fcc07-120">System.String</span></span>

## <span data-ttu-id="fcc07-121">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="fcc07-121">OUTPUTS</span></span>

### <span data-ttu-id="fcc07-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="fcc07-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="fcc07-123">NOTES</span><span class="sxs-lookup"><span data-stu-id="fcc07-123">NOTES</span></span>

## <span data-ttu-id="fcc07-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fcc07-124">RELATED LINKS</span></span>

[<span data-ttu-id="fcc07-125">Set-AzDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="fcc07-125">Set-AzDtlVMsPerUserPolicy</span></span>](./Set-AzDtlVMsPerUserPolicy.md)


