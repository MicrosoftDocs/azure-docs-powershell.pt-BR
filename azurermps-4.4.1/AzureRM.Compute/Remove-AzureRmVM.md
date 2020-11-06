---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: A16C2084-30A4-4AB8-AE22-28CC6E74FD48
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVM.md
ms.openlocfilehash: 3cc48d103867008b247ce480de43d1ccadc68d18
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432638"
---
# <span data-ttu-id="ad7ed-101">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ad7ed-101">Remove-AzureRmVM</span></span>

## <span data-ttu-id="ad7ed-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ad7ed-102">SYNOPSIS</span></span>
<span data-ttu-id="ad7ed-103">Remove uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="ad7ed-103">Removes a virtual machine from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad7ed-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ad7ed-104">SYNTAX</span></span>

### <span data-ttu-id="ad7ed-105">ResourceGroupNameParameterSetName (padrão)</span><span class="sxs-lookup"><span data-stu-id="ad7ed-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Remove-AzureRmVM [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad7ed-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="ad7ed-106">IdParameterSetName</span></span>
```
Remove-AzureRmVM [-Name] <String> [-Force] [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad7ed-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ad7ed-107">DESCRIPTION</span></span>
<span data-ttu-id="ad7ed-108">O cmdlet **Remove-AzureRmVM** remove uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="ad7ed-108">The **Remove-AzureRmVM** cmdlet removes a virtual machine from Azure.</span></span>

## <span data-ttu-id="ad7ed-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ad7ed-109">EXAMPLES</span></span>

### <span data-ttu-id="ad7ed-110">Exemplo 1: remover uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="ad7ed-110">Example 1: Remove a virtual machine</span></span>
```
PS C:\> Remove-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="ad7ed-111">Esse comando Remove a máquina virtual nomeada VirtualMachine07 na ResourceGroup11 do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ad7ed-111">This command removes the virtual machine named VirtualMachine07 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="ad7ed-112">OS</span><span class="sxs-lookup"><span data-stu-id="ad7ed-112">PARAMETERS</span></span>

### <span data-ttu-id="ad7ed-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad7ed-113">-DefaultProfile</span></span>
<span data-ttu-id="ad7ed-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ad7ed-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad7ed-115">-Force</span><span class="sxs-lookup"><span data-stu-id="ad7ed-115">-Force</span></span>
<span data-ttu-id="ad7ed-116">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="ad7ed-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad7ed-117">-ID</span><span class="sxs-lookup"><span data-stu-id="ad7ed-117">-Id</span></span>
<span data-ttu-id="ad7ed-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ad7ed-118">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad7ed-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="ad7ed-119">-Name</span></span>
<span data-ttu-id="ad7ed-120">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="ad7ed-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad7ed-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad7ed-121">-ResourceGroupName</span></span>
<span data-ttu-id="ad7ed-122">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ad7ed-122">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad7ed-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ad7ed-123">-Confirm</span></span>
<span data-ttu-id="ad7ed-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad7ed-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad7ed-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad7ed-125">-WhatIf</span></span>
<span data-ttu-id="ad7ed-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ad7ed-126">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="ad7ed-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ad7ed-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad7ed-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad7ed-128">CommonParameters</span></span>
<span data-ttu-id="ad7ed-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad7ed-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad7ed-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad7ed-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad7ed-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ad7ed-131">INPUTS</span></span>

## <span data-ttu-id="ad7ed-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ad7ed-132">OUTPUTS</span></span>

## <span data-ttu-id="ad7ed-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ad7ed-133">NOTES</span></span>

## <span data-ttu-id="ad7ed-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ad7ed-134">RELATED LINKS</span></span>

[<span data-ttu-id="ad7ed-135">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ad7ed-135">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="ad7ed-136">New-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ad7ed-136">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="ad7ed-137">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ad7ed-137">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="ad7ed-138">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ad7ed-138">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="ad7ed-139">Parar-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ad7ed-139">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="ad7ed-140">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ad7ed-140">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


