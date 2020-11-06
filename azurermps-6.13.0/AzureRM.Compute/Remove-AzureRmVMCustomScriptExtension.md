---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: A65E82D5-706B-4470-A51E-936E381DA78F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmcustomscriptextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVMCustomScriptExtension.md
ms.openlocfilehash: ee0762dfa78a5bd863ede7b56cb746c2c8cab3be
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610623"
---
# <span data-ttu-id="abaa1-101">Remove-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="abaa1-101">Remove-AzureRmVMCustomScriptExtension</span></span>

## <span data-ttu-id="abaa1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="abaa1-102">SYNOPSIS</span></span>
<span data-ttu-id="abaa1-103">Remove uma extensão de script personalizada de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="abaa1-103">Removes a custom script extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="abaa1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="abaa1-104">SYNTAX</span></span>

```
Remove-AzureRmVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="abaa1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="abaa1-105">DESCRIPTION</span></span>
<span data-ttu-id="abaa1-106">O cmdlet **Remove-AzureRmVMCustomScriptExtension** remove uma extensão de máquina virtual de script personalizada de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="abaa1-106">The **Remove-AzureRmVMCustomScriptExtension** cmdlet removes a custom script Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="abaa1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="abaa1-107">EXAMPLES</span></span>

## <span data-ttu-id="abaa1-108">OS</span><span class="sxs-lookup"><span data-stu-id="abaa1-108">PARAMETERS</span></span>

### <span data-ttu-id="abaa1-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abaa1-109">-DefaultProfile</span></span>
<span data-ttu-id="abaa1-110">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="abaa1-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="abaa1-111">-Force</span><span class="sxs-lookup"><span data-stu-id="abaa1-111">-Force</span></span>
<span data-ttu-id="abaa1-112">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="abaa1-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abaa1-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="abaa1-113">-Name</span></span>
<span data-ttu-id="abaa1-114">Especifica o nome da extensão de script personalizada que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="abaa1-114">Specifies the name of the custom script extension that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abaa1-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="abaa1-115">-ResourceGroupName</span></span>
<span data-ttu-id="abaa1-116">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="abaa1-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="abaa1-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="abaa1-117">-VMName</span></span>
<span data-ttu-id="abaa1-118">Especifica o nome de uma máquina virtual a partir da qual esse cmdlet Remove a extensão de script personalizada.</span><span class="sxs-lookup"><span data-stu-id="abaa1-118">Specifies the name of a virtual machine from which this cmdlet removes the custom script extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abaa1-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="abaa1-119">-Confirm</span></span>
<span data-ttu-id="abaa1-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="abaa1-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="abaa1-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="abaa1-121">-WhatIf</span></span>
<span data-ttu-id="abaa1-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="abaa1-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="abaa1-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="abaa1-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="abaa1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abaa1-124">CommonParameters</span></span>
<span data-ttu-id="abaa1-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="abaa1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abaa1-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="abaa1-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abaa1-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="abaa1-127">INPUTS</span></span>

### <span data-ttu-id="abaa1-128">System. String</span><span class="sxs-lookup"><span data-stu-id="abaa1-128">System.String</span></span>

## <span data-ttu-id="abaa1-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="abaa1-129">OUTPUTS</span></span>

### <span data-ttu-id="abaa1-130">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="abaa1-130">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="abaa1-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="abaa1-131">NOTES</span></span>

## <span data-ttu-id="abaa1-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="abaa1-132">RELATED LINKS</span></span>

[<span data-ttu-id="abaa1-133">Get-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="abaa1-133">Get-AzureRmVMCustomScriptExtension</span></span>](./Get-AzureRmVMCustomScriptExtension.md)

[<span data-ttu-id="abaa1-134">Set-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="abaa1-134">Set-AzureRmVMCustomScriptExtension</span></span>](./Set-AzureRmVMCustomScriptExtension.md)
