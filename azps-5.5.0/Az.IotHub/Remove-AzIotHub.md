---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHub.md
ms.openlocfilehash: 4e851c6a65e2ff69e6675a2e057a1ed319ba6519
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116739"
---
# <span data-ttu-id="f9fcc-101">Remove-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="f9fcc-101">Remove-AzIotHub</span></span>

## <span data-ttu-id="f9fcc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f9fcc-102">SYNOPSIS</span></span>
<span data-ttu-id="f9fcc-103">Exclui um IotHub.</span><span class="sxs-lookup"><span data-stu-id="f9fcc-103">Deletes an IotHub.</span></span>

## <span data-ttu-id="f9fcc-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f9fcc-104">SYNTAX</span></span>

```
Remove-AzIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9fcc-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="f9fcc-105">DESCRIPTION</span></span>
<span data-ttu-id="f9fcc-106">Exclui um IotHub.</span><span class="sxs-lookup"><span data-stu-id="f9fcc-106">Deletes an IotHub.</span></span>

## <span data-ttu-id="f9fcc-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f9fcc-107">EXAMPLES</span></span>

### <span data-ttu-id="f9fcc-108">Exemplo 1 Remover um IotHub</span><span class="sxs-lookup"><span data-stu-id="f9fcc-108">Example 1 Remove an IotHub</span></span>
```
PS C:\> Remove-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="f9fcc-109">Remove um IotHub chamado "myiothub"</span><span class="sxs-lookup"><span data-stu-id="f9fcc-109">Removes an IotHub named "myiothub"</span></span>

## <span data-ttu-id="f9fcc-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f9fcc-110">PARAMETERS</span></span>

### <span data-ttu-id="f9fcc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9fcc-111">-DefaultProfile</span></span>
<span data-ttu-id="f9fcc-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="f9fcc-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f9fcc-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="f9fcc-113">-Name</span></span>
<span data-ttu-id="f9fcc-114">Nome do IotHub</span><span class="sxs-lookup"><span data-stu-id="f9fcc-114">Name of the IotHub</span></span>

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

### <span data-ttu-id="f9fcc-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9fcc-115">-ResourceGroupName</span></span>
<span data-ttu-id="f9fcc-116">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="f9fcc-116">Resource Group Name</span></span>

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

### <span data-ttu-id="f9fcc-117">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="f9fcc-117">-Confirm</span></span>
<span data-ttu-id="f9fcc-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f9fcc-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9fcc-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9fcc-119">-WhatIf</span></span>
<span data-ttu-id="f9fcc-120">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="f9fcc-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9fcc-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f9fcc-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9fcc-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9fcc-122">CommonParameters</span></span>
<span data-ttu-id="f9fcc-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9fcc-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9fcc-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9fcc-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9fcc-125">Entradas</span><span class="sxs-lookup"><span data-stu-id="f9fcc-125">INPUTS</span></span>

### <span data-ttu-id="f9fcc-126">System.String</span><span class="sxs-lookup"><span data-stu-id="f9fcc-126">System.String</span></span>

## <span data-ttu-id="f9fcc-127">Saídas</span><span class="sxs-lookup"><span data-stu-id="f9fcc-127">OUTPUTS</span></span>

### <span data-ttu-id="f9fcc-128">System.Void</span><span class="sxs-lookup"><span data-stu-id="f9fcc-128">System.Void</span></span>

## <span data-ttu-id="f9fcc-129">Notas</span><span class="sxs-lookup"><span data-stu-id="f9fcc-129">NOTES</span></span>

## <span data-ttu-id="f9fcc-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f9fcc-130">RELATED LINKS</span></span>
