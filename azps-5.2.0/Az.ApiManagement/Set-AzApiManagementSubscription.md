---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 52115C49-0229-4F2C-B7B0-02FC52C1D32D
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementSubscription.md
ms.openlocfilehash: 82c49524566293adcd8dcbdcb36359e83360158c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98261141"
---
# <span data-ttu-id="a6500-101">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="a6500-101">Set-AzApiManagementSubscription</span></span>

## <span data-ttu-id="a6500-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a6500-102">SYNOPSIS</span></span>
<span data-ttu-id="a6500-103">Define detalhes de assinatura existentes.</span><span class="sxs-lookup"><span data-stu-id="a6500-103">Sets existing subscription details.</span></span>

## <span data-ttu-id="a6500-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a6500-104">SYNTAX</span></span>

### <span data-ttu-id="a6500-105">ByInputObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="a6500-105">ByInputObject (Default)</span></span>
```
Set-AzApiManagementSubscription -InputObject <PsApiManagementSubscription> [-Scope <String>] [-UserId <String>]
 [-Name <String>] [-PrimaryKey <String>] [-SecondaryKey <String>] [-State <PsApiManagementSubscriptionState>]
 [-ExpiresOn <DateTime>] [-StateComment <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6500-106">ExpandedParameter</span><span class="sxs-lookup"><span data-stu-id="a6500-106">ExpandedParameter</span></span>
```
Set-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String> [-Scope <String>]
 [-UserId <String>] [-Name <String>] [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-State <PsApiManagementSubscriptionState>] [-ExpiresOn <DateTime>] [-StateComment <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6500-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a6500-107">DESCRIPTION</span></span>
<span data-ttu-id="a6500-108">O cmdlet **set-AzApiManagementSubscription** define os detalhes da assinatura existente.</span><span class="sxs-lookup"><span data-stu-id="a6500-108">The **Set-AzApiManagementSubscription** cmdlet sets existing subscription details.</span></span>

## <span data-ttu-id="a6500-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a6500-109">EXAMPLES</span></span>

### <span data-ttu-id="a6500-110">Exemplo 1: definir o estado e as chaves primárias e secundárias para uma assinatura</span><span class="sxs-lookup"><span data-stu-id="a6500-110">Example 1: Set the state and primary and secondary keys for a subscription</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementSubscription -Context $apimContext -SubscriptionId -0123456789 -PrimaryKey "80450f7d0b6d481382113073f67822c1" -SecondaryKey "97d6112c3a8f48d5bf0266b7a09a761c" -State "Active"
```

<span data-ttu-id="a6500-111">Este comando define as chaves primária e secundária para uma assinatura e a ativa.</span><span class="sxs-lookup"><span data-stu-id="a6500-111">This command sets the primary and secondary keys for a subscription and activates it.</span></span>

## <span data-ttu-id="a6500-112">OS</span><span class="sxs-lookup"><span data-stu-id="a6500-112">PARAMETERS</span></span>

### <span data-ttu-id="a6500-113">-Contexto</span><span class="sxs-lookup"><span data-stu-id="a6500-113">-Context</span></span>
<span data-ttu-id="a6500-114">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="a6500-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="a6500-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6500-115">-DefaultProfile</span></span>
<span data-ttu-id="a6500-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a6500-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a6500-117">-ExpiresOn</span><span class="sxs-lookup"><span data-stu-id="a6500-117">-ExpiresOn</span></span>
<span data-ttu-id="a6500-118">Especifica uma data de validade da assinatura.</span><span class="sxs-lookup"><span data-stu-id="a6500-118">Specifies a subscription expiration date.</span></span>
<span data-ttu-id="a6500-119">O valor padrão desse parâmetro é $Null.</span><span class="sxs-lookup"><span data-stu-id="a6500-119">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="a6500-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a6500-120">-InputObject</span></span>
<span data-ttu-id="a6500-121">Instância do PsApiManagementSubscription.</span><span class="sxs-lookup"><span data-stu-id="a6500-121">Instance of PsApiManagementSubscription.</span></span> <span data-ttu-id="a6500-122">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="a6500-122">This parameter is required.</span></span>

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

### <span data-ttu-id="a6500-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="a6500-123">-Name</span></span>
<span data-ttu-id="a6500-124">Especifica um nome de assinatura.</span><span class="sxs-lookup"><span data-stu-id="a6500-124">Specifies a subscription name.</span></span>

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

### <span data-ttu-id="a6500-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a6500-125">-PassThru</span></span>
<span data-ttu-id="a6500-126">PassThru</span><span class="sxs-lookup"><span data-stu-id="a6500-126">passthru</span></span>

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

### <span data-ttu-id="a6500-127">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="a6500-127">-PrimaryKey</span></span>
<span data-ttu-id="a6500-128">Especifica a chave primária de assinatura.</span><span class="sxs-lookup"><span data-stu-id="a6500-128">Specifies the subscription primary key.</span></span>
<span data-ttu-id="a6500-129">Esse parâmetro é gerado automaticamente se não for especificado.</span><span class="sxs-lookup"><span data-stu-id="a6500-129">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="a6500-130">Esse parâmetro deve ter de 1 a 300 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="a6500-130">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="a6500-131">-Escopo</span><span class="sxs-lookup"><span data-stu-id="a6500-131">-Scope</span></span>
<span data-ttu-id="a6500-132">O escopo da assinatura, seja o escopo da API/apis/{apiId} ou o escopo do produto/products/{productId} ou o escopo da API global/APIs ou escopo global/.</span><span class="sxs-lookup"><span data-stu-id="a6500-132">The Scope of the Subscription, whether it is Api Scope /apis/{apiId} or Product Scope /products/{productId} or Global API Scope /apis or Global scope /.</span></span> <span data-ttu-id="a6500-133">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="a6500-133">This parameter is required.</span></span>

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

### <span data-ttu-id="a6500-134">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="a6500-134">-SecondaryKey</span></span>
<span data-ttu-id="a6500-135">Especifica a chave secundária de assinatura.</span><span class="sxs-lookup"><span data-stu-id="a6500-135">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="a6500-136">Esse parâmetro é gerado automaticamente se não for especificado.</span><span class="sxs-lookup"><span data-stu-id="a6500-136">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="a6500-137">Esse parâmetro deve ter de 1 a 300 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="a6500-137">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="a6500-138">-Estado</span><span class="sxs-lookup"><span data-stu-id="a6500-138">-State</span></span>
<span data-ttu-id="a6500-139">Especifica o estado da assinatura.</span><span class="sxs-lookup"><span data-stu-id="a6500-139">Specifies the subscription state.</span></span>
<span data-ttu-id="a6500-140">O valor padrão desse parâmetro é $Null.</span><span class="sxs-lookup"><span data-stu-id="a6500-140">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="a6500-141">-StateComment</span><span class="sxs-lookup"><span data-stu-id="a6500-141">-StateComment</span></span>
<span data-ttu-id="a6500-142">Especifica o comentário do estado da assinatura.</span><span class="sxs-lookup"><span data-stu-id="a6500-142">Specifies the subscription state comment.</span></span>
<span data-ttu-id="a6500-143">O valor padrão desse parâmetro é $Null.</span><span class="sxs-lookup"><span data-stu-id="a6500-143">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="a6500-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a6500-144">-SubscriptionId</span></span>
<span data-ttu-id="a6500-145">Especifica a ID da assinatura.</span><span class="sxs-lookup"><span data-stu-id="a6500-145">Specifies the subscription ID.</span></span>

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

### <span data-ttu-id="a6500-146">-UserId</span><span class="sxs-lookup"><span data-stu-id="a6500-146">-UserId</span></span>
<span data-ttu-id="a6500-147">O proprietário da assinatura.</span><span class="sxs-lookup"><span data-stu-id="a6500-147">The owner of the subscription.</span></span> <span data-ttu-id="a6500-148">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="a6500-148">This parameter is optional.</span></span>

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

### <span data-ttu-id="a6500-149">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a6500-149">-Confirm</span></span>
<span data-ttu-id="a6500-150">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6500-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6500-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6500-151">-WhatIf</span></span>
<span data-ttu-id="a6500-152">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a6500-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a6500-153">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a6500-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6500-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6500-154">CommonParameters</span></span>
<span data-ttu-id="a6500-155">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6500-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6500-156">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a6500-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6500-157">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a6500-157">INPUTS</span></span>

### <span data-ttu-id="a6500-158">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="a6500-158">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a6500-159">System. String</span><span class="sxs-lookup"><span data-stu-id="a6500-159">System.String</span></span>

### <span data-ttu-id="a6500-160">System. Nullable ' 1 [[Microsoft. Azure. Commands. ApiManagement. Management. Models. PsApiManagementSubscriptionState, Microsoft. Azure. PowerShell. cmdlets. ApiManagement. immanagement, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="a6500-160">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="a6500-161">System. Nullable ' 1 [[System. DateTime, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="a6500-161">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="a6500-162">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a6500-162">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a6500-163">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a6500-163">OUTPUTS</span></span>

### <span data-ttu-id="a6500-164">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="a6500-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="a6500-165">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a6500-165">NOTES</span></span>

## <span data-ttu-id="a6500-166">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a6500-166">RELATED LINKS</span></span>

[<span data-ttu-id="a6500-167">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="a6500-167">Get-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="a6500-168">New-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="a6500-168">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="a6500-169">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="a6500-169">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)


