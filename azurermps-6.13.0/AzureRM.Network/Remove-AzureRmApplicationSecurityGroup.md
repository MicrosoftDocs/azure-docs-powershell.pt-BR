---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationSecurityGroup.md
ms.openlocfilehash: a1d0935e7ca61d5eee3055ad9751fd794e093e8d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427227"
---
# <span data-ttu-id="a136e-101">Remove-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a136e-101">Remove-AzureRmApplicationSecurityGroup</span></span>

## <span data-ttu-id="a136e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a136e-102">SYNOPSIS</span></span>
<span data-ttu-id="a136e-103">Remove um grupo de segurança de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a136e-103">Removes an application security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a136e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a136e-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationSecurityGroup -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a136e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a136e-105">DESCRIPTION</span></span>
<span data-ttu-id="a136e-106">O cmdlet **Remove-AzureRmApplicationSecurityGroup** remove um grupo de segurança de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a136e-106">The **Remove-AzureRmApplicationSecurityGroup** cmdlet removes an application security group.</span></span>

## <span data-ttu-id="a136e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a136e-107">EXAMPLES</span></span>

### <span data-ttu-id="a136e-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a136e-108">Example 1</span></span>
```
PS C:\>Remove-AzureRmApplicationSecurityGroup -Name "MyApplicationSecurityGrouo" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="a136e-109">Esse comando exclui um grupo de segurança de aplicativo chamado MyApplicationSecurityGrouo no grupo de recursos chamado MyResource Group.</span><span class="sxs-lookup"><span data-stu-id="a136e-109">This command deletes an application security group named MyApplicationSecurityGrouo in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="a136e-110">OS</span><span class="sxs-lookup"><span data-stu-id="a136e-110">PARAMETERS</span></span>

### <span data-ttu-id="a136e-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a136e-111">-AsJob</span></span>
<span data-ttu-id="a136e-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="a136e-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a136e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a136e-113">-DefaultProfile</span></span>
<span data-ttu-id="a136e-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a136e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a136e-115">-Force</span><span class="sxs-lookup"><span data-stu-id="a136e-115">-Force</span></span>
<span data-ttu-id="a136e-116">Não pedir confirmação se quiser excluir o recurso</span><span class="sxs-lookup"><span data-stu-id="a136e-116">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="a136e-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="a136e-117">-Name</span></span>
<span data-ttu-id="a136e-118">O nome do grupo de segurança do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a136e-118">The name of the application security group.</span></span>

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

### <span data-ttu-id="a136e-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a136e-119">-PassThru</span></span>
<span data-ttu-id="a136e-120">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="a136e-120">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="a136e-121">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="a136e-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a136e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a136e-122">-ResourceGroupName</span></span>
<span data-ttu-id="a136e-123">O nome do grupo de recursos do grupo de segurança do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a136e-123">The resource group name of the application security group.</span></span>

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

### <span data-ttu-id="a136e-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a136e-124">-Confirm</span></span>
<span data-ttu-id="a136e-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a136e-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a136e-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a136e-126">-WhatIf</span></span>
<span data-ttu-id="a136e-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a136e-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a136e-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a136e-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a136e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a136e-129">CommonParameters</span></span>
<span data-ttu-id="a136e-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a136e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a136e-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a136e-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a136e-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a136e-132">INPUTS</span></span>

### <span data-ttu-id="a136e-133">System. String</span><span class="sxs-lookup"><span data-stu-id="a136e-133">System.String</span></span>

## <span data-ttu-id="a136e-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a136e-134">OUTPUTS</span></span>

### <span data-ttu-id="a136e-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a136e-135">System.Boolean</span></span>

## <span data-ttu-id="a136e-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a136e-136">NOTES</span></span>

## <span data-ttu-id="a136e-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a136e-137">RELATED LINKS</span></span>

[<span data-ttu-id="a136e-138">New-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a136e-138">New-AzureRmApplicationSecurityGroup</span></span>](./New-AzureRmApplicationSecurityGroup.md)

[<span data-ttu-id="a136e-139">Get-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a136e-139">Get-AzureRmApplicationSecurityGroup</span></span>](./Get-AzureRmApplicationSecurityGroup.md)
