---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/remove-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Remove-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Remove-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 1f0f3a9986f69be082a91606d07e86d493f4a269
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112706"
---
# <span data-ttu-id="42719-101">Remove-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="42719-101">Remove-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="42719-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="42719-102">SYNOPSIS</span></span>
<span data-ttu-id="42719-103">Exclui uma instância da Capacidade Inserida do PowerBI.</span><span class="sxs-lookup"><span data-stu-id="42719-103">Deletes an instance of PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="42719-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="42719-104">SYNTAX</span></span>

### <span data-ttu-id="42719-105">ByNameAndResourceGroup (Padrão)</span><span class="sxs-lookup"><span data-stu-id="42719-105">ByNameAndResourceGroup (Default)</span></span>
```
Remove-AzPowerBIEmbeddedCapacity [-Name] <String> [-ResourceGroupName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42719-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="42719-106">ByResourceId</span></span>
```
Remove-AzPowerBIEmbeddedCapacity [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42719-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="42719-107">ByInputObject</span></span>
```
Remove-AzPowerBIEmbeddedCapacity [-InputObject] <PSPowerBIEmbeddedCapacity> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42719-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="42719-108">DESCRIPTION</span></span>
<span data-ttu-id="42719-109">O Remove-AzPowerBIEmbeddedCapacity cmdlet exclui uma instância da Capacidade Inserida do PowerBI</span><span class="sxs-lookup"><span data-stu-id="42719-109">The Remove-AzPowerBIEmbeddedCapacity cmdlet deletes an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="42719-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="42719-110">EXAMPLES</span></span>

### <span data-ttu-id="42719-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="42719-111">Example 1</span></span>
```
PS C:\> Remove-AzPowerBIEmbeddedCapacity -Name "testcapacity" -ResourceGroupName "testRG"
Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/testcapacity
ResourceGroup          : testRG
Name                   : testcapacity
Location               : West Central US
State                  : Succeeded
Administrator          : {admin@microsoft.com}
Sku                    : A1
Tier                   : PBIE_Azure
Tag                    : {}
```

<span data-ttu-id="42719-112">Esse comando removerá a capacidade nomeada de testcapacity no testeRG do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="42719-112">This command will remove the capacity named testcapacity in the resourcegroup testRG</span></span>

## <span data-ttu-id="42719-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="42719-113">PARAMETERS</span></span>

### <span data-ttu-id="42719-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42719-114">-DefaultProfile</span></span>
<span data-ttu-id="42719-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="42719-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42719-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="42719-116">-InputObject</span></span>
<span data-ttu-id="42719-117">Objeto de entrada para Piping</span><span class="sxs-lookup"><span data-stu-id="42719-117">Input object for Piping</span></span>

```yaml
Type: Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="42719-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="42719-118">-Name</span></span>
<span data-ttu-id="42719-119">Nome da Capacidade Inserida do PowerBI</span><span class="sxs-lookup"><span data-stu-id="42719-119">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42719-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="42719-120">-PassThru</span></span>
<span data-ttu-id="42719-121">Retornará os detalhes da capacidade excluída se a operação for concluída com êxito</span><span class="sxs-lookup"><span data-stu-id="42719-121">Will return the deleted capacity details if the operation completes successfully</span></span>

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

### <span data-ttu-id="42719-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42719-122">-ResourceGroupName</span></span>
<span data-ttu-id="42719-123">Nome do grupo de recursos do Azure ao qual a capacidade pertence</span><span class="sxs-lookup"><span data-stu-id="42719-123">Name of the Azure resource group to which the capacity belongs</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42719-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="42719-124">-ResourceId</span></span>
<span data-ttu-id="42719-125">ID de recurso do Azure</span><span class="sxs-lookup"><span data-stu-id="42719-125">Azure resource ID</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42719-126">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="42719-126">-Confirm</span></span>
<span data-ttu-id="42719-127">Solicita que o usuário confirme se a operação será realizada</span><span class="sxs-lookup"><span data-stu-id="42719-127">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="42719-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42719-128">-WhatIf</span></span>
<span data-ttu-id="42719-129">Descreve as ações que a operação atual executará sem realmente executa-las</span><span class="sxs-lookup"><span data-stu-id="42719-129">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="42719-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42719-130">CommonParameters</span></span>
<span data-ttu-id="42719-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42719-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42719-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42719-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42719-133">Entradas</span><span class="sxs-lookup"><span data-stu-id="42719-133">INPUTS</span></span>

### <span data-ttu-id="42719-134">System.String</span><span class="sxs-lookup"><span data-stu-id="42719-134">System.String</span></span>

### <span data-ttu-id="42719-135">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="42719-135">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="42719-136">Saídas</span><span class="sxs-lookup"><span data-stu-id="42719-136">OUTPUTS</span></span>

### <span data-ttu-id="42719-137">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="42719-137">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="42719-138">Notas</span><span class="sxs-lookup"><span data-stu-id="42719-138">NOTES</span></span>

## <span data-ttu-id="42719-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="42719-139">RELATED LINKS</span></span>

[<span data-ttu-id="42719-140">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="42719-140">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="42719-141">New-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="42719-141">New-AzPowerBIEmbeddedCapacity</span></span>](./New-AzPowerBIEmbeddedCapacity.md)
