---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 6C40A7BA-6BE2-464A-84E4-9021935A5BF6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMExtension.md
ms.openlocfilehash: 164fdd36ca0e97dde33caec1322ddfa2bb6a15c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426965"
---
# <span data-ttu-id="3a590-101">Remove-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="3a590-101">Remove-AzureRmVMExtension</span></span>

## <span data-ttu-id="3a590-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3a590-102">SYNOPSIS</span></span>
<span data-ttu-id="3a590-103">Remove uma extensão de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="3a590-103">Removes an extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3a590-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3a590-104">SYNTAX</span></span>

```
Remove-AzureRmVMExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a590-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3a590-105">DESCRIPTION</span></span>
<span data-ttu-id="3a590-106">O cmdlet **Remove-AzureRmVMExtension** remove uma extensão das extensões de máquina virtual de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="3a590-106">The **Remove-AzureRmVMExtension** cmdlet removes an extension from the Virtual Machine Extensions of a virtual machine.</span></span>

## <span data-ttu-id="3a590-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3a590-107">EXAMPLES</span></span>

### <span data-ttu-id="3a590-108">Exemplo 1: remover uma extensão de uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="3a590-108">Example 1: Remove an extension from a virtual machine</span></span>
```
PS C:\> Remove-AzureRmVMExtension -ResourceGroupName "ResourceGroup11" -Name "ContosoTest" -VMName "VirtualMachine22"
```

<span data-ttu-id="3a590-109">Esse comando Remove a extensão chamada ContosoTest da máquina virtual nomeada VirtualMachine22 em ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="3a590-109">This command removes the extension named ContosoTest from the virtual machine named VirtualMachine22 in ResourceGroup11.</span></span>

## <span data-ttu-id="3a590-110">OS</span><span class="sxs-lookup"><span data-stu-id="3a590-110">PARAMETERS</span></span>

### <span data-ttu-id="3a590-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a590-111">-DefaultProfile</span></span>
<span data-ttu-id="3a590-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3a590-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3a590-113">-Force</span><span class="sxs-lookup"><span data-stu-id="3a590-113">-Force</span></span>
<span data-ttu-id="3a590-114">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="3a590-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3a590-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="3a590-115">-Name</span></span>
<span data-ttu-id="3a590-116">Especifica o nome da extensão que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="3a590-116">Specifies the name of the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="3a590-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a590-117">-ResourceGroupName</span></span>
<span data-ttu-id="3a590-118">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="3a590-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="3a590-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="3a590-119">-VMName</span></span>
<span data-ttu-id="3a590-120">Especifica o nome de uma máquina virtual a partir da qual esse cmdlet Remove a extensão.</span><span class="sxs-lookup"><span data-stu-id="3a590-120">Specifies the name of a virtual machine from which this cmdlet removes the extension.</span></span>

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

### <span data-ttu-id="3a590-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3a590-121">-Confirm</span></span>
<span data-ttu-id="3a590-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a590-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a590-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a590-123">-WhatIf</span></span>
<span data-ttu-id="3a590-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3a590-124">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="3a590-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3a590-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a590-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a590-126">CommonParameters</span></span>
<span data-ttu-id="3a590-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a590-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a590-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a590-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a590-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3a590-129">INPUTS</span></span>

## <span data-ttu-id="3a590-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3a590-130">OUTPUTS</span></span>

## <span data-ttu-id="3a590-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3a590-131">NOTES</span></span>

## <span data-ttu-id="3a590-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3a590-132">RELATED LINKS</span></span>

[<span data-ttu-id="3a590-133">Get-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="3a590-133">Get-AzureRmVMExtension</span></span>](./Get-AzureRmVMExtension.md)

[<span data-ttu-id="3a590-134">Set-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="3a590-134">Set-AzureRmVMExtension</span></span>](./Set-AzureRmVMExtension.md)


