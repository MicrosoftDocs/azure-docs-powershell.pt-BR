---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: F6D9EA59-BA61-4117-8771-9B190424BFF8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/set-azurermintegrationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccount.md
ms.openlocfilehash: c6f86d31f97ac0f4fcdbdd45c6bc111eda045800
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602604"
---
# <span data-ttu-id="16a49-101">Set-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="16a49-101">Set-AzureRmIntegrationAccount</span></span>

## <span data-ttu-id="16a49-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="16a49-102">SYNOPSIS</span></span>
<span data-ttu-id="16a49-103">Modifica uma conta de integração.</span><span class="sxs-lookup"><span data-stu-id="16a49-103">Modifies an integration account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="16a49-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="16a49-104">SYNTAX</span></span>

```
Set-AzureRmIntegrationAccount -ResourceGroupName <String> -Name <String> [-Location <String>] [-Sku <String>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16a49-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="16a49-105">DESCRIPTION</span></span>
<span data-ttu-id="16a49-106">O cmdlet **set-AzureRmIntegrationAccount** modifica uma conta de integração.</span><span class="sxs-lookup"><span data-stu-id="16a49-106">The **Set-AzureRmIntegrationAccount** cmdlet modifies an integration account.</span></span>
<span data-ttu-id="16a49-107">Esse cmdlet retorna um objeto que representa a conta de integração.</span><span class="sxs-lookup"><span data-stu-id="16a49-107">This cmdlet returns an object that represents the integration account.</span></span>
<span data-ttu-id="16a49-108">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="16a49-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="16a49-109">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="16a49-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="16a49-110">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e, em seguida, pressione a tecla TAB repetidamente para percorrer os parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="16a49-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="16a49-111">Se você omitir um parâmetro de modelo obrigatório, o cmdlet solicitará que você tenha o valor.</span><span class="sxs-lookup"><span data-stu-id="16a49-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="16a49-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="16a49-112">EXAMPLES</span></span>

### <span data-ttu-id="16a49-113">Exemplo 1: modificar uma conta de integração</span><span class="sxs-lookup"><span data-stu-id="16a49-113">Example 1: Modify an integration account</span></span>
```
PS C:\>Set-AzureRmIntegrationAccount -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -Sku "Free"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="16a49-114">Esse comando modifica uma conta de integração chamada IntegrationAccount31 no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="16a49-114">This command modifies an integration account named IntegrationAccount31 in the specified resource group.</span></span>

## <span data-ttu-id="16a49-115">OS</span><span class="sxs-lookup"><span data-stu-id="16a49-115">PARAMETERS</span></span>

### <span data-ttu-id="16a49-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16a49-116">-DefaultProfile</span></span>
<span data-ttu-id="16a49-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="16a49-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="16a49-118">-Force</span><span class="sxs-lookup"><span data-stu-id="16a49-118">-Force</span></span>
<span data-ttu-id="16a49-119">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="16a49-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="16a49-120">-Local</span><span class="sxs-lookup"><span data-stu-id="16a49-120">-Location</span></span>
<span data-ttu-id="16a49-121">Especifica um local para a conta de integração.</span><span class="sxs-lookup"><span data-stu-id="16a49-121">Specifies a location for the integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16a49-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="16a49-122">-Name</span></span>
<span data-ttu-id="16a49-123">Especifica o nome da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="16a49-123">Specifies the name of the integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16a49-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16a49-124">-ResourceGroupName</span></span>
<span data-ttu-id="16a49-125">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="16a49-125">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="16a49-126">-SKU</span><span class="sxs-lookup"><span data-stu-id="16a49-126">-Sku</span></span>
<span data-ttu-id="16a49-127">Especifica um nome de SKU para a conta de integração.</span><span class="sxs-lookup"><span data-stu-id="16a49-127">Specifies a SKU name for the integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16a49-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="16a49-128">-Confirm</span></span>
<span data-ttu-id="16a49-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="16a49-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16a49-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16a49-130">-WhatIf</span></span>
<span data-ttu-id="16a49-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="16a49-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16a49-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="16a49-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16a49-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16a49-133">CommonParameters</span></span>
<span data-ttu-id="16a49-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16a49-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16a49-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16a49-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16a49-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="16a49-136">INPUTS</span></span>

### <span data-ttu-id="16a49-137">System. String</span><span class="sxs-lookup"><span data-stu-id="16a49-137">System.String</span></span>

## <span data-ttu-id="16a49-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="16a49-138">OUTPUTS</span></span>

### <span data-ttu-id="16a49-139">Microsoft. Azure. Management. Logic. Models. IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="16a49-139">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

## <span data-ttu-id="16a49-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="16a49-140">NOTES</span></span>

## <span data-ttu-id="16a49-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="16a49-141">RELATED LINKS</span></span>

[<span data-ttu-id="16a49-142">Get-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="16a49-142">Get-AzureRmIntegrationAccount</span></span>](./Get-AzureRmIntegrationAccount.md)

[<span data-ttu-id="16a49-143">New-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="16a49-143">New-AzureRmIntegrationAccount</span></span>](./New-AzureRmIntegrationAccount.md)

[<span data-ttu-id="16a49-144">Remove-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="16a49-144">Remove-AzureRmIntegrationAccount</span></span>](./Remove-AzureRmIntegrationAccount.md)


