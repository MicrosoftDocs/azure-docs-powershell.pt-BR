---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: A3F653C7-6F9D-4B2B-81F8-0A012D80ECC7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devtestlabs/get-azurermdtlvmsperlabpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlVMsPerLabPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlVMsPerLabPolicy.md
ms.openlocfilehash: 83b061c646d8d6f75689d6a67fe163c43456edb1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429799"
---
# <span data-ttu-id="dc5a7-101">Get-AzureRmDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="dc5a7-101">Get-AzureRmDtlVMsPerLabPolicy</span></span>

## <span data-ttu-id="dc5a7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dc5a7-102">SYNOPSIS</span></span>
<span data-ttu-id="dc5a7-103">Obtém a política de máquinas virtuais por laboratório de um laboratório no DevTest Labs.</span><span class="sxs-lookup"><span data-stu-id="dc5a7-103">Gets the virtual machines per lab policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dc5a7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dc5a7-104">SYNTAX</span></span>

```
Get-AzureRmDtlVMsPerLabPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dc5a7-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dc5a7-105">DESCRIPTION</span></span>
<span data-ttu-id="dc5a7-106">O cmdlet **Get-AzureRmDtlVMsPerLabPolicy** Obtém as máquinas virtuais por política de laboratório de um laboratório, que permite definir o número total de máquinas virtuais permitidas em um laboratório.</span><span class="sxs-lookup"><span data-stu-id="dc5a7-106">The **Get-AzureRmDtlVMsPerLabPolicy** cmdlet gets the virtual machines per lab policy of a lab, which allows you set the total number of virtual machines allowed in a lab.</span></span>
<span data-ttu-id="dc5a7-107">O cmdlet retorna o status habilitado ou desabilitado da política e o número total de máquinas virtuais permitidas no laboratório que você definiu na política.</span><span class="sxs-lookup"><span data-stu-id="dc5a7-107">The cmdlet returns the enabled or disabled status of the policy, and the total number of virtual machines allowed in the lab that you have set in the policy.</span></span>

## <span data-ttu-id="dc5a7-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dc5a7-108">EXAMPLES</span></span>

## <span data-ttu-id="dc5a7-109">OS</span><span class="sxs-lookup"><span data-stu-id="dc5a7-109">PARAMETERS</span></span>

### <span data-ttu-id="dc5a7-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc5a7-110">-DefaultProfile</span></span>
<span data-ttu-id="dc5a7-111">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="dc5a7-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dc5a7-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="dc5a7-112">-LabName</span></span>
<span data-ttu-id="dc5a7-113">Especifica o nome do laboratório para o qual esse cmdlet obtém as máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="dc5a7-113">Specifies the name of the lab for which this cmdlet gets the virtual machines.</span></span>

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

### <span data-ttu-id="dc5a7-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc5a7-114">-ResourceGroupName</span></span>
<span data-ttu-id="dc5a7-115">Especifica o nome do grupo de recursos ao qual o laboratório pertence.</span><span class="sxs-lookup"><span data-stu-id="dc5a7-115">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="dc5a7-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc5a7-116">CommonParameters</span></span>
<span data-ttu-id="dc5a7-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc5a7-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc5a7-118">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc5a7-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc5a7-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dc5a7-119">INPUTS</span></span>

### <span data-ttu-id="dc5a7-120">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="dc5a7-120">None</span></span>
<span data-ttu-id="dc5a7-121">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="dc5a7-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="dc5a7-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dc5a7-122">OUTPUTS</span></span>

### <span data-ttu-id="dc5a7-123">Microsoft. Azure. Commands. DevTestLabs. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="dc5a7-123">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>
<span data-ttu-id="dc5a7-124">Esse cmdlet retorna a política que especifica o número máximo de máquinas virtuais que podem ser criadas no laboratório.</span><span class="sxs-lookup"><span data-stu-id="dc5a7-124">This cmdlet returns the policy that specifies the maximum number of virtual machines that can be created in the lab.</span></span>

## <span data-ttu-id="dc5a7-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dc5a7-125">NOTES</span></span>

## <span data-ttu-id="dc5a7-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dc5a7-126">RELATED LINKS</span></span>

[<span data-ttu-id="dc5a7-127">Set-AzureRmDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="dc5a7-127">Set-AzureRmDtlVMsPerLabPolicy</span></span>](./Set-AzureRmDtlVMsPerLabPolicy.md)


