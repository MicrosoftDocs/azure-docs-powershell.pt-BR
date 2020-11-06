---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 56550997-21D9-4F85-B23A-677625482547
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/remove-azurermintegrationaccountschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountSchema.md
ms.openlocfilehash: 2600928a21548a4af49d3d7453b04cc2c505feb8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430902"
---
# <span data-ttu-id="b1684-101">Remove-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="b1684-101">Remove-AzureRmIntegrationAccountSchema</span></span>

## <span data-ttu-id="b1684-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b1684-102">SYNOPSIS</span></span>
<span data-ttu-id="b1684-103">Remove um esquema de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="b1684-103">Removes an integration account schema.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b1684-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b1684-104">SYNTAX</span></span>

```
Remove-AzureRmIntegrationAccountSchema -ResourceGroupName <String> -Name <String> -SchemaName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1684-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b1684-105">DESCRIPTION</span></span>
<span data-ttu-id="b1684-106">O cmdlet **Remove-AzureRmIntegrationAccountSchema** remove um esquema de conta de integração de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b1684-106">The **Remove-AzureRmIntegrationAccountSchema** cmdlet removes an integration account schema from a resource group.</span></span>
<span data-ttu-id="b1684-107">Especificando o nome da conta de integração, o nome do grupo de recursos e o nome do esquema.</span><span class="sxs-lookup"><span data-stu-id="b1684-107">Specifying the integration account name, resource group name, and schema name.</span></span>
<span data-ttu-id="b1684-108">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="b1684-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="b1684-109">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="b1684-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="b1684-110">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e, em seguida, pressione a tecla TAB repetidamente para percorrer os parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="b1684-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="b1684-111">Se você omitir um parâmetro de modelo obrigatório, o cmdlet solicitará que você tenha o valor.</span><span class="sxs-lookup"><span data-stu-id="b1684-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="b1684-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b1684-112">EXAMPLES</span></span>

### <span data-ttu-id="b1684-113">Exemplo 1: remover um esquema de conta de integração</span><span class="sxs-lookup"><span data-stu-id="b1684-113">Example 1: Remove an integration account schema</span></span>
```
PS C:\>Remove-AzureRmIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -SchemaName "IntegrationAccountSchema43"
```

<span data-ttu-id="b1684-114">Esse comando Remove um esquema de conta de integração chamado IntegrationAccountSchema43.</span><span class="sxs-lookup"><span data-stu-id="b1684-114">This command removes an integration account schema named IntegrationAccountSchema43.</span></span>

## <span data-ttu-id="b1684-115">OS</span><span class="sxs-lookup"><span data-stu-id="b1684-115">PARAMETERS</span></span>

### <span data-ttu-id="b1684-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1684-116">-DefaultProfile</span></span>
<span data-ttu-id="b1684-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="b1684-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b1684-118">-Force</span><span class="sxs-lookup"><span data-stu-id="b1684-118">-Force</span></span>
<span data-ttu-id="b1684-119">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="b1684-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b1684-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="b1684-120">-Name</span></span>
<span data-ttu-id="b1684-121">Especifica o nome da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="b1684-121">Specifies the name of the integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1684-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1684-122">-ResourceGroupName</span></span>
<span data-ttu-id="b1684-123">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b1684-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="b1684-124">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="b1684-124">-SchemaName</span></span>
<span data-ttu-id="b1684-125">Especifica o nome de um esquema de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="b1684-125">Specifies the name of an integration account schema.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1684-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b1684-126">-Confirm</span></span>
<span data-ttu-id="b1684-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1684-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1684-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1684-128">-WhatIf</span></span>
<span data-ttu-id="b1684-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b1684-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1684-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b1684-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1684-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1684-131">CommonParameters</span></span>
<span data-ttu-id="b1684-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1684-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1684-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1684-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1684-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b1684-134">INPUTS</span></span>

### <span data-ttu-id="b1684-135">System. String</span><span class="sxs-lookup"><span data-stu-id="b1684-135">System.String</span></span>

## <span data-ttu-id="b1684-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b1684-136">OUTPUTS</span></span>

### <span data-ttu-id="b1684-137">System. void</span><span class="sxs-lookup"><span data-stu-id="b1684-137">System.Void</span></span>

## <span data-ttu-id="b1684-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b1684-138">NOTES</span></span>

## <span data-ttu-id="b1684-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b1684-139">RELATED LINKS</span></span>

[<span data-ttu-id="b1684-140">Get-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="b1684-140">Get-AzureRmIntegrationAccountSchema</span></span>](./Get-AzureRmIntegrationAccountSchema.md)

[<span data-ttu-id="b1684-141">New-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="b1684-141">New-AzureRmIntegrationAccountSchema</span></span>](./New-AzureRmIntegrationAccountSchema.md)

[<span data-ttu-id="b1684-142">Set-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="b1684-142">Set-AzureRmIntegrationAccountSchema</span></span>](./Set-AzureRmIntegrationAccountSchema.md)

