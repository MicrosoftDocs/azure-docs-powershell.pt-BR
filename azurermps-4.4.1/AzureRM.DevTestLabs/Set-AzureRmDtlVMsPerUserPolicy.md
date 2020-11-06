---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: D00E04D9-C91F-4F89-8867-0A026C274F27
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlVMsPerUserPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlVMsPerUserPolicy.md
ms.openlocfilehash: b3790105f2404cc7bf50ef1200ce0978e8f0b15d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433136"
---
# <span data-ttu-id="55e5c-101">Set-AzureRmDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="55e5c-101">Set-AzureRmDtlVMsPerUserPolicy</span></span>

## <span data-ttu-id="55e5c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="55e5c-102">SYNOPSIS</span></span>
<span data-ttu-id="55e5c-103">Define a política de máquinas virtuais por usuário de um laboratório no DevTest Labs.</span><span class="sxs-lookup"><span data-stu-id="55e5c-103">Sets the virtual machines per user policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="55e5c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="55e5c-104">SYNTAX</span></span>

### <span data-ttu-id="55e5c-105">Habilitar (padrão)</span><span class="sxs-lookup"><span data-stu-id="55e5c-105">Enable (Default)</span></span>
```
Set-AzureRmDtlVMsPerUserPolicy [[-MaxVMs] <Int32>] [-Enable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55e5c-106">Desabilita</span><span class="sxs-lookup"><span data-stu-id="55e5c-106">Disable</span></span>
```
Set-AzureRmDtlVMsPerUserPolicy [[-MaxVMs] <Int32>] [-Disable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55e5c-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="55e5c-107">DESCRIPTION</span></span>
<span data-ttu-id="55e5c-108">O cmdlet **set-AzureRmDtlVMsPerUserPolicy** define a política de máquinas virtuais por usuário de um laboratório, que define o número máximo de máquinas virtuais permitidas por usuário.</span><span class="sxs-lookup"><span data-stu-id="55e5c-108">The **Set-AzureRmDtlVMsPerUserPolicy** cmdlet sets the virtual machines per user policy of a lab, which sets the maximum number of virtual machines allowed per user.</span></span>
<span data-ttu-id="55e5c-109">O cmdlet usa o grupo de recursos e o nome do laboratório especificado para definir a política.</span><span class="sxs-lookup"><span data-stu-id="55e5c-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="55e5c-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="55e5c-110">EXAMPLES</span></span>

## <span data-ttu-id="55e5c-111">OS</span><span class="sxs-lookup"><span data-stu-id="55e5c-111">PARAMETERS</span></span>

### <span data-ttu-id="55e5c-112">-Disable</span><span class="sxs-lookup"><span data-stu-id="55e5c-112">-Disable</span></span>
<span data-ttu-id="55e5c-113">Indica que esse cmdlet desabilita a política do laboratório.</span><span class="sxs-lookup"><span data-stu-id="55e5c-113">Indicates that this cmdlet disables the policy for the lab.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Disable
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55e5c-114">-Habilitar</span><span class="sxs-lookup"><span data-stu-id="55e5c-114">-Enable</span></span>
<span data-ttu-id="55e5c-115">Indica que esse cmdlet habilita a política para o laboratório.</span><span class="sxs-lookup"><span data-stu-id="55e5c-115">Indicates that this cmdlet enables the policy for the lab.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Enable
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55e5c-116">-LabName</span><span class="sxs-lookup"><span data-stu-id="55e5c-116">-LabName</span></span>
<span data-ttu-id="55e5c-117">Especifica o nome do laboratório para o qual esse cmdlet define a política de máquinas virtuais por usuário.</span><span class="sxs-lookup"><span data-stu-id="55e5c-117">Specifies the name of the lab for which this cmdlet sets the virtual machines per user policy.</span></span>

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

### <span data-ttu-id="55e5c-118">-MaxVMs</span><span class="sxs-lookup"><span data-stu-id="55e5c-118">-MaxVMs</span></span>
<span data-ttu-id="55e5c-119">Especifica o número máximo de máquinas virtuais que podem ser criadas no laboratório.</span><span class="sxs-lookup"><span data-stu-id="55e5c-119">Specifies the maximum number of virtual machines that can be created in the lab.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55e5c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55e5c-120">-ResourceGroupName</span></span>
<span data-ttu-id="55e5c-121">Especifica o nome do grupo de recursos ao qual o laboratório pertence.</span><span class="sxs-lookup"><span data-stu-id="55e5c-121">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="55e5c-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="55e5c-122">-Confirm</span></span>
<span data-ttu-id="55e5c-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="55e5c-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55e5c-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55e5c-124">-WhatIf</span></span>
<span data-ttu-id="55e5c-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="55e5c-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55e5c-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="55e5c-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55e5c-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55e5c-127">-DefaultProfile</span></span>
<span data-ttu-id="55e5c-128">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="55e5c-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55e5c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55e5c-129">CommonParameters</span></span>
<span data-ttu-id="55e5c-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55e5c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55e5c-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55e5c-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55e5c-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="55e5c-132">INPUTS</span></span>

## <span data-ttu-id="55e5c-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="55e5c-133">OUTPUTS</span></span>

### <span data-ttu-id="55e5c-134">Microsoft. Azure. Commands. DevTestLabs. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="55e5c-134">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>
<span data-ttu-id="55e5c-135">Esse cmdlet retorna a política que especifica o número máximo de máquinas virtuais que podem ser criadas por um usuário no laboratório.</span><span class="sxs-lookup"><span data-stu-id="55e5c-135">This cmdlet returns the policy that specifies the maximum number of virtual machines that can be created by a user in the lab.</span></span>

## <span data-ttu-id="55e5c-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="55e5c-136">NOTES</span></span>

## <span data-ttu-id="55e5c-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="55e5c-137">RELATED LINKS</span></span>

[<span data-ttu-id="55e5c-138">Get-AzureRmDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="55e5c-138">Get-AzureRmDtlVMsPerUserPolicy</span></span>](./Get-AzureRmDtlVMsPerUserPolicy.md)


