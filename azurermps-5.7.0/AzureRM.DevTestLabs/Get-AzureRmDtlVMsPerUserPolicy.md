---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: 5029179A-99A5-4350-A8E5-D15ABA59CC93
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devtestlabs/get-azurermdtlvmsperuserpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlVMsPerUserPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlVMsPerUserPolicy.md
ms.openlocfilehash: 53afed94f9733c041df2c49ff1ec97a2fb8277f0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428929"
---
# <span data-ttu-id="6ec35-101">Get-AzureRmDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="6ec35-101">Get-AzureRmDtlVMsPerUserPolicy</span></span>

## <span data-ttu-id="6ec35-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6ec35-102">SYNOPSIS</span></span>
<span data-ttu-id="6ec35-103">Obtém a política de máquinas virtuais por usuário de um laboratório no DevTest Labs.</span><span class="sxs-lookup"><span data-stu-id="6ec35-103">Gets the virtual machines per user policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6ec35-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6ec35-104">SYNTAX</span></span>

```
Get-AzureRmDtlVMsPerUserPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ec35-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6ec35-105">DESCRIPTION</span></span>
<span data-ttu-id="6ec35-106">O cmdlet **Get-AzureRmDtlVMsPerUserPolicy** Obtém a política de máquinas virtuais por usuário de um laboratório, que permite definir o número máximo de máquinas virtuais permitidas por usuário.</span><span class="sxs-lookup"><span data-stu-id="6ec35-106">The **Get-AzureRmDtlVMsPerUserPolicy** cmdlet gets the virtual machines per user policy of a lab, which allows you to set the maximum number of virtual machines allowed per user.</span></span>
<span data-ttu-id="6ec35-107">O cmdlet retorna o status habilitado ou desabilitado da política e o número máximo de máquinas virtuais permitidas por usuário que você definiu na política.</span><span class="sxs-lookup"><span data-stu-id="6ec35-107">The cmdlet returns the enabled or disabled status of the policy and the maximum number of virtual machines allowed per user that you have set in the policy.</span></span>

## <span data-ttu-id="6ec35-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6ec35-108">EXAMPLES</span></span>

## <span data-ttu-id="6ec35-109">OS</span><span class="sxs-lookup"><span data-stu-id="6ec35-109">PARAMETERS</span></span>

### <span data-ttu-id="6ec35-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ec35-110">-DefaultProfile</span></span>
<span data-ttu-id="6ec35-111">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="6ec35-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6ec35-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="6ec35-112">-LabName</span></span>
<span data-ttu-id="6ec35-113">Especifica o nome do laboratório para o qual esse cmdlet obtém a política por usuário da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="6ec35-113">Specifies the name of the lab for which this cmdlet gets the virtual machine per user policy.</span></span>

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

### <span data-ttu-id="6ec35-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ec35-114">-ResourceGroupName</span></span>
<span data-ttu-id="6ec35-115">Especifica o nome do grupo de recursos ao qual o laboratório pertence.</span><span class="sxs-lookup"><span data-stu-id="6ec35-115">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="6ec35-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ec35-116">CommonParameters</span></span>
<span data-ttu-id="6ec35-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ec35-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ec35-118">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ec35-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ec35-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6ec35-119">INPUTS</span></span>

### <span data-ttu-id="6ec35-120">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="6ec35-120">None</span></span>
<span data-ttu-id="6ec35-121">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="6ec35-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6ec35-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6ec35-122">OUTPUTS</span></span>

### <span data-ttu-id="6ec35-123">Microsoft. Azure. Commands. DevTestLabs. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="6ec35-123">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>
<span data-ttu-id="6ec35-124">Esse cmdlet retorna a política que especifica o número máximo de máquinas virtuais que podem ser criadas por um usuário no laboratório.</span><span class="sxs-lookup"><span data-stu-id="6ec35-124">This cmdlet returns the policy that specifies the maximum number of virtual machines that can be created by a user in the lab.</span></span>

## <span data-ttu-id="6ec35-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6ec35-125">NOTES</span></span>

## <span data-ttu-id="6ec35-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6ec35-126">RELATED LINKS</span></span>

[<span data-ttu-id="6ec35-127">Set-AzureRmDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="6ec35-127">Set-AzureRmDtlVMsPerUserPolicy</span></span>](./Set-AzureRmDtlVMsPerUserPolicy.md)


