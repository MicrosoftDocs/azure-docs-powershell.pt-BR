---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 52115C49-0229-4F2C-B7B0-02FC52C1D32D
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementSubscription.md
ms.openlocfilehash: 82c49524566293adcd8dcbdcb36359e83360158c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100127149"
---
# <span data-ttu-id="7adbb-101">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="7adbb-101">Set-AzApiManagementSubscription</span></span>

## <span data-ttu-id="7adbb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7adbb-102">SYNOPSIS</span></span>
<span data-ttu-id="7adbb-103">Define os detalhes da assinatura existentes.</span><span class="sxs-lookup"><span data-stu-id="7adbb-103">Sets existing subscription details.</span></span>

## <span data-ttu-id="7adbb-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7adbb-104">SYNTAX</span></span>

### <span data-ttu-id="7adbb-105">ByInputObject (Padrão)</span><span class="sxs-lookup"><span data-stu-id="7adbb-105">ByInputObject (Default)</span></span>
```
Set-AzApiManagementSubscription -InputObject <PsApiManagementSubscription> [-Scope <String>] [-UserId <String>]
 [-Name <String>] [-PrimaryKey <String>] [-SecondaryKey <String>] [-State <PsApiManagementSubscriptionState>]
 [-ExpiresOn <DateTime>] [-StateComment <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7adbb-106">ExpandedParameter</span><span class="sxs-lookup"><span data-stu-id="7adbb-106">ExpandedParameter</span></span>
```
Set-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String> [-Scope <String>]
 [-UserId <String>] [-Name <String>] [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-State <PsApiManagementSubscriptionState>] [-ExpiresOn <DateTime>] [-StateComment <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7adbb-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="7adbb-107">DESCRIPTION</span></span>
<span data-ttu-id="7adbb-108">O **cmdlet Set-AzApiManagementSubscription define** os detalhes de assinatura existentes.</span><span class="sxs-lookup"><span data-stu-id="7adbb-108">The **Set-AzApiManagementSubscription** cmdlet sets existing subscription details.</span></span>

## <span data-ttu-id="7adbb-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7adbb-109">EXAMPLES</span></span>

### <span data-ttu-id="7adbb-110">Exemplo 1: Definir o estado e as chaves primárias e secundárias para uma assinatura</span><span class="sxs-lookup"><span data-stu-id="7adbb-110">Example 1: Set the state and primary and secondary keys for a subscription</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementSubscription -Context $apimContext -SubscriptionId -0123456789 -PrimaryKey "80450f7d0b6d481382113073f67822c1" -SecondaryKey "97d6112c3a8f48d5bf0266b7a09a761c" -State "Active"
```

<span data-ttu-id="7adbb-111">Esse comando define as chaves primária e secundária de uma assinatura e a ativa.</span><span class="sxs-lookup"><span data-stu-id="7adbb-111">This command sets the primary and secondary keys for a subscription and activates it.</span></span>

## <span data-ttu-id="7adbb-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7adbb-112">PARAMETERS</span></span>

### <span data-ttu-id="7adbb-113">-Contexto</span><span class="sxs-lookup"><span data-stu-id="7adbb-113">-Context</span></span>
<span data-ttu-id="7adbb-114">Especifica um **objeto PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="7adbb-114">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7adbb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7adbb-115">-DefaultProfile</span></span>
<span data-ttu-id="7adbb-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="7adbb-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7adbb-117">-ExpiresOn</span><span class="sxs-lookup"><span data-stu-id="7adbb-117">-ExpiresOn</span></span>
<span data-ttu-id="7adbb-118">Especifica a data de vencimento de uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="7adbb-118">Specifies a subscription expiration date.</span></span>
<span data-ttu-id="7adbb-119">O valor padrão deste parâmetro é $Null.</span><span class="sxs-lookup"><span data-stu-id="7adbb-119">The default value of this parameter is $Null.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7adbb-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7adbb-120">-InputObject</span></span>
<span data-ttu-id="7adbb-121">Instância de PsApiManagementSubscription.</span><span class="sxs-lookup"><span data-stu-id="7adbb-121">Instance of PsApiManagementSubscription.</span></span> <span data-ttu-id="7adbb-122">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="7adbb-122">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7adbb-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="7adbb-123">-Name</span></span>
<span data-ttu-id="7adbb-124">Especifica o nome de uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="7adbb-124">Specifies a subscription name.</span></span>

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

### <span data-ttu-id="7adbb-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7adbb-125">-PassThru</span></span>
<span data-ttu-id="7adbb-126">Passthru</span><span class="sxs-lookup"><span data-stu-id="7adbb-126">passthru</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7adbb-127">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="7adbb-127">-PrimaryKey</span></span>
<span data-ttu-id="7adbb-128">Especifica a chave primária da assinatura.</span><span class="sxs-lookup"><span data-stu-id="7adbb-128">Specifies the subscription primary key.</span></span>
<span data-ttu-id="7adbb-129">Esse parâmetro é gerado automaticamente, se não especificado.</span><span class="sxs-lookup"><span data-stu-id="7adbb-129">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="7adbb-130">Esse parâmetro deve ter de 1 a 300 caracteres.</span><span class="sxs-lookup"><span data-stu-id="7adbb-130">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="7adbb-131">-Escopo</span><span class="sxs-lookup"><span data-stu-id="7adbb-131">-Scope</span></span>
<span data-ttu-id="7adbb-132">O Escopo da Assinatura, seja o Escopo da Api /apis/{apiId} ou Escopo do Produto /products/{productId} ou Escopo da API Global /apis ou escopo global /.</span><span class="sxs-lookup"><span data-stu-id="7adbb-132">The Scope of the Subscription, whether it is Api Scope /apis/{apiId} or Product Scope /products/{productId} or Global API Scope /apis or Global scope /.</span></span> <span data-ttu-id="7adbb-133">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="7adbb-133">This parameter is required.</span></span>

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

### <span data-ttu-id="7adbb-134">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="7adbb-134">-SecondaryKey</span></span>
<span data-ttu-id="7adbb-135">Especifica a chave secundária da assinatura.</span><span class="sxs-lookup"><span data-stu-id="7adbb-135">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="7adbb-136">Esse parâmetro é gerado automaticamente, se não especificado.</span><span class="sxs-lookup"><span data-stu-id="7adbb-136">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="7adbb-137">Esse parâmetro deve ter de 1 a 300 caracteres.</span><span class="sxs-lookup"><span data-stu-id="7adbb-137">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="7adbb-138">-Estado</span><span class="sxs-lookup"><span data-stu-id="7adbb-138">-State</span></span>
<span data-ttu-id="7adbb-139">Especifica o estado da assinatura.</span><span class="sxs-lookup"><span data-stu-id="7adbb-139">Specifies the subscription state.</span></span>
<span data-ttu-id="7adbb-140">O valor padrão deste parâmetro é $Null.</span><span class="sxs-lookup"><span data-stu-id="7adbb-140">The default value of this parameter is $Null.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState]
Parameter Sets: (All)
Aliases:
Accepted values: Suspended, Active, Expired, Submitted, Rejected, Cancelled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7adbb-141">-StateComment</span><span class="sxs-lookup"><span data-stu-id="7adbb-141">-StateComment</span></span>
<span data-ttu-id="7adbb-142">Especifica o comentário do estado da assinatura.</span><span class="sxs-lookup"><span data-stu-id="7adbb-142">Specifies the subscription state comment.</span></span>
<span data-ttu-id="7adbb-143">O valor padrão deste parâmetro é $Null.</span><span class="sxs-lookup"><span data-stu-id="7adbb-143">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="7adbb-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7adbb-144">-SubscriptionId</span></span>
<span data-ttu-id="7adbb-145">Especifica a ID da assinatura.</span><span class="sxs-lookup"><span data-stu-id="7adbb-145">Specifies the subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7adbb-146">-UserId</span><span class="sxs-lookup"><span data-stu-id="7adbb-146">-UserId</span></span>
<span data-ttu-id="7adbb-147">O proprietário da assinatura.</span><span class="sxs-lookup"><span data-stu-id="7adbb-147">The owner of the subscription.</span></span> <span data-ttu-id="7adbb-148">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="7adbb-148">This parameter is optional.</span></span>

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

### <span data-ttu-id="7adbb-149">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="7adbb-149">-Confirm</span></span>
<span data-ttu-id="7adbb-150">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7adbb-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7adbb-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7adbb-151">-WhatIf</span></span>
<span data-ttu-id="7adbb-152">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="7adbb-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7adbb-153">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7adbb-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7adbb-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7adbb-154">CommonParameters</span></span>
<span data-ttu-id="7adbb-155">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7adbb-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7adbb-156">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7adbb-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7adbb-157">Entradas</span><span class="sxs-lookup"><span data-stu-id="7adbb-157">INPUTS</span></span>

### <span data-ttu-id="7adbb-158">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="7adbb-158">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="7adbb-159">System.String</span><span class="sxs-lookup"><span data-stu-id="7adbb-159">System.String</span></span>

### <span data-ttu-id="7adbb-160">System.Nullable'1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0,0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="7adbb-160">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="7adbb-161">System.Nullable'1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="7adbb-161">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="7adbb-162">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7adbb-162">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7adbb-163">Saídas</span><span class="sxs-lookup"><span data-stu-id="7adbb-163">OUTPUTS</span></span>

### <span data-ttu-id="7adbb-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="7adbb-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="7adbb-165">Notas</span><span class="sxs-lookup"><span data-stu-id="7adbb-165">NOTES</span></span>

## <span data-ttu-id="7adbb-166">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7adbb-166">RELATED LINKS</span></span>

[<span data-ttu-id="7adbb-167">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="7adbb-167">Get-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="7adbb-168">New-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="7adbb-168">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="7adbb-169">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="7adbb-169">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)


