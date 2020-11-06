---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: F6D9EA59-BA61-4117-8771-9B190424BFF8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccount.md
ms.openlocfilehash: 3861e4bdc9c61f1e08664f90fd6efbf8ddcedab4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609652"
---
# <span data-ttu-id="29507-101">Set-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="29507-101">Set-AzureRmIntegrationAccount</span></span>

## <span data-ttu-id="29507-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="29507-102">SYNOPSIS</span></span>
<span data-ttu-id="29507-103">Modifica uma conta de integração.</span><span class="sxs-lookup"><span data-stu-id="29507-103">Modifies an integration account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="29507-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="29507-104">SYNTAX</span></span>

```
Set-AzureRmIntegrationAccount -ResourceGroupName <String> -Name <String> [-Location <String>] [-Sku <String>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29507-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="29507-105">DESCRIPTION</span></span>
<span data-ttu-id="29507-106">O cmdlet **set-AzureRmIntegrationAccount** modifica uma conta de integração.</span><span class="sxs-lookup"><span data-stu-id="29507-106">The **Set-AzureRmIntegrationAccount** cmdlet modifies an integration account.</span></span>
<span data-ttu-id="29507-107">Esse cmdlet retorna um objeto que representa a conta de integração.</span><span class="sxs-lookup"><span data-stu-id="29507-107">This cmdlet returns an object that represents the integration account.</span></span>

<span data-ttu-id="29507-108">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="29507-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="29507-109">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="29507-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="29507-110">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e, em seguida, pressione a tecla TAB repetidamente para percorrer os parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="29507-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="29507-111">Se você omitir um parâmetro de modelo obrigatório, o cmdlet solicitará que você tenha o valor.</span><span class="sxs-lookup"><span data-stu-id="29507-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="29507-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="29507-112">EXAMPLES</span></span>

### <span data-ttu-id="29507-113">Exemplo 1: modificar uma conta de integração</span><span class="sxs-lookup"><span data-stu-id="29507-113">Example 1: Modify an integration account</span></span>
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

<span data-ttu-id="29507-114">Esse comando modifica uma conta de integração chamada IntegrationAccount31 no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="29507-114">This command modifies an integration account named IntegrationAccount31 in the specified resource group.</span></span>

## <span data-ttu-id="29507-115">OS</span><span class="sxs-lookup"><span data-stu-id="29507-115">PARAMETERS</span></span>

### <span data-ttu-id="29507-116">-Force</span><span class="sxs-lookup"><span data-stu-id="29507-116">-Force</span></span>
<span data-ttu-id="29507-117">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="29507-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="29507-118">-Local</span><span class="sxs-lookup"><span data-stu-id="29507-118">-Location</span></span>
<span data-ttu-id="29507-119">Especifica um local para a conta de integração.</span><span class="sxs-lookup"><span data-stu-id="29507-119">Specifies a location for the integration account.</span></span>

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

### <span data-ttu-id="29507-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="29507-120">-Name</span></span>
<span data-ttu-id="29507-121">Especifica o nome da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="29507-121">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="29507-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29507-122">-ResourceGroupName</span></span>
<span data-ttu-id="29507-123">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="29507-123">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="29507-124">-SKU</span><span class="sxs-lookup"><span data-stu-id="29507-124">-Sku</span></span>
<span data-ttu-id="29507-125">Especifica um nome de SKU para a conta de integração.</span><span class="sxs-lookup"><span data-stu-id="29507-125">Specifies a SKU name for the integration account.</span></span>

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

### <span data-ttu-id="29507-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="29507-126">-Confirm</span></span>
<span data-ttu-id="29507-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="29507-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29507-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29507-128">-WhatIf</span></span>
<span data-ttu-id="29507-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="29507-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29507-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="29507-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29507-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29507-131">-DefaultProfile</span></span>
<span data-ttu-id="29507-132">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="29507-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="29507-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29507-133">CommonParameters</span></span>
<span data-ttu-id="29507-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29507-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29507-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29507-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29507-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="29507-136">INPUTS</span></span>

## <span data-ttu-id="29507-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="29507-137">OUTPUTS</span></span>

### <span data-ttu-id="29507-138">Microsoft. Azure. Management. Logic. Models. IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="29507-138">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

## <span data-ttu-id="29507-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="29507-139">NOTES</span></span>

## <span data-ttu-id="29507-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="29507-140">RELATED LINKS</span></span>

[<span data-ttu-id="29507-141">Get-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="29507-141">Get-AzureRmIntegrationAccount</span></span>](./Get-AzureRmIntegrationAccount.md)

[<span data-ttu-id="29507-142">New-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="29507-142">New-AzureRmIntegrationAccount</span></span>](./New-AzureRmIntegrationAccount.md)

[<span data-ttu-id="29507-143">Remove-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="29507-143">Remove-AzureRmIntegrationAccount</span></span>](./Remove-AzureRmIntegrationAccount.md)


