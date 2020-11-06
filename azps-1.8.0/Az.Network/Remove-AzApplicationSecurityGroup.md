---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationSecurityGroup.md
ms.openlocfilehash: 0af35c08cce181ba96f15ca77c0f17f96cfeb32e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93600190"
---
# <span data-ttu-id="54c9c-101">Remove-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="54c9c-101">Remove-AzApplicationSecurityGroup</span></span>

## <span data-ttu-id="54c9c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="54c9c-102">SYNOPSIS</span></span>
<span data-ttu-id="54c9c-103">Remove um grupo de segurança de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="54c9c-103">Removes an application security group.</span></span>

## <span data-ttu-id="54c9c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="54c9c-104">SYNTAX</span></span>

```
Remove-AzApplicationSecurityGroup -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54c9c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="54c9c-105">DESCRIPTION</span></span>
<span data-ttu-id="54c9c-106">O cmdlet **Remove-AzApplicationSecurityGroup** remove um grupo de segurança de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="54c9c-106">The **Remove-AzApplicationSecurityGroup** cmdlet removes an application security group.</span></span>

## <span data-ttu-id="54c9c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="54c9c-107">EXAMPLES</span></span>

### <span data-ttu-id="54c9c-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="54c9c-108">Example 1</span></span>
```
PS C:\>Remove-AzApplicationSecurityGroup -Name "MyApplicationSecurityGrouo" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="54c9c-109">Esse comando exclui um grupo de segurança de aplicativo chamado MyApplicationSecurityGrouo no grupo de recursos chamado MyResource Group.</span><span class="sxs-lookup"><span data-stu-id="54c9c-109">This command deletes an application security group named MyApplicationSecurityGrouo in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="54c9c-110">OS</span><span class="sxs-lookup"><span data-stu-id="54c9c-110">PARAMETERS</span></span>

### <span data-ttu-id="54c9c-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="54c9c-111">-AsJob</span></span>
<span data-ttu-id="54c9c-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="54c9c-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="54c9c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54c9c-113">-DefaultProfile</span></span>
<span data-ttu-id="54c9c-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="54c9c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54c9c-115">-Force</span><span class="sxs-lookup"><span data-stu-id="54c9c-115">-Force</span></span>
<span data-ttu-id="54c9c-116">Não pedir confirmação se quiser excluir o recurso</span><span class="sxs-lookup"><span data-stu-id="54c9c-116">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="54c9c-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="54c9c-117">-Name</span></span>
<span data-ttu-id="54c9c-118">O nome do grupo de segurança do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="54c9c-118">The name of the application security group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54c9c-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="54c9c-119">-PassThru</span></span>
<span data-ttu-id="54c9c-120">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="54c9c-120">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="54c9c-121">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="54c9c-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="54c9c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54c9c-122">-ResourceGroupName</span></span>
<span data-ttu-id="54c9c-123">O nome do grupo de recursos do grupo de segurança do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="54c9c-123">The resource group name of the application security group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54c9c-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="54c9c-124">-Confirm</span></span>
<span data-ttu-id="54c9c-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="54c9c-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54c9c-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54c9c-126">-WhatIf</span></span>
<span data-ttu-id="54c9c-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="54c9c-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54c9c-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="54c9c-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54c9c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54c9c-129">CommonParameters</span></span>
<span data-ttu-id="54c9c-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54c9c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54c9c-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54c9c-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54c9c-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="54c9c-132">INPUTS</span></span>

### <span data-ttu-id="54c9c-133">System. String</span><span class="sxs-lookup"><span data-stu-id="54c9c-133">System.String</span></span>

## <span data-ttu-id="54c9c-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="54c9c-134">OUTPUTS</span></span>

### <span data-ttu-id="54c9c-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="54c9c-135">System.Boolean</span></span>

## <span data-ttu-id="54c9c-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="54c9c-136">NOTES</span></span>

## <span data-ttu-id="54c9c-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="54c9c-137">RELATED LINKS</span></span>

[<span data-ttu-id="54c9c-138">New-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="54c9c-138">New-AzApplicationSecurityGroup</span></span>](./New-AzApplicationSecurityGroup.md)

[<span data-ttu-id="54c9c-139">Get-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="54c9c-139">Get-AzApplicationSecurityGroup</span></span>](./Get-AzApplicationSecurityGroup.md)
