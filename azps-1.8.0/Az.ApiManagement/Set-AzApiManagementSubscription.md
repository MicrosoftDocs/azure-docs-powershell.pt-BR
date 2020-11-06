---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 52115C49-0229-4F2C-B7B0-02FC52C1D32D
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementSubscription.md
ms.openlocfilehash: cbdc876368f55ace6f77c04172dc2f0a53b0a7f6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93601666"
---
# <span data-ttu-id="cbf0e-101">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="cbf0e-101">Set-AzApiManagementSubscription</span></span>

## <span data-ttu-id="cbf0e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cbf0e-102">SYNOPSIS</span></span>
<span data-ttu-id="cbf0e-103">Define detalhes de assinatura existentes.</span><span class="sxs-lookup"><span data-stu-id="cbf0e-103">Sets existing subscription details.</span></span>

## <span data-ttu-id="cbf0e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cbf0e-104">SYNTAX</span></span>

```
Set-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String> [-Name <String>]
 [-PrimaryKey <String>] [-SecondaryKey <String>] [-State <PsApiManagementSubscriptionState>]
 [-ExpiresOn <DateTime>] [-StateComment <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cbf0e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cbf0e-105">DESCRIPTION</span></span>
<span data-ttu-id="cbf0e-106">O cmdlet **set-AzApiManagementSubscription** define os detalhes da assinatura existente.</span><span class="sxs-lookup"><span data-stu-id="cbf0e-106">The **Set-AzApiManagementSubscription** cmdlet sets existing subscription details.</span></span>

## <span data-ttu-id="cbf0e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cbf0e-107">EXAMPLES</span></span>

### <span data-ttu-id="cbf0e-108">Exemplo 1: definir o estado e as chaves primárias e secundárias para uma assinatura</span><span class="sxs-lookup"><span data-stu-id="cbf0e-108">Example 1: Set the state and primary and secondary keys for a subscription</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementSubscription -Context $apimContext -SubscriptionId -0123456789 -PrimaryKey "80450f7d0b6d481382113073f67822c1" -SecondaryKey "97d6112c3a8f48d5bf0266b7a09a761c" -State "Active"
```

<span data-ttu-id="cbf0e-109">Este comando define as chaves primária e secundária para uma assinatura e a ativa.</span><span class="sxs-lookup"><span data-stu-id="cbf0e-109">This command sets the primary and secondary keys for a subscription and activates it.</span></span>

## <span data-ttu-id="cbf0e-110">OS</span><span class="sxs-lookup"><span data-stu-id="cbf0e-110">PARAMETERS</span></span>

### <span data-ttu-id="cbf0e-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="cbf0e-111">-Context</span></span>
<span data-ttu-id="cbf0e-112">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="cbf0e-112">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cbf0e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbf0e-113">-DefaultProfile</span></span>
<span data-ttu-id="cbf0e-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cbf0e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cbf0e-115">-ExpiresOn</span><span class="sxs-lookup"><span data-stu-id="cbf0e-115">-ExpiresOn</span></span>
<span data-ttu-id="cbf0e-116">Especifica uma data de validade da assinatura.</span><span class="sxs-lookup"><span data-stu-id="cbf0e-116">Specifies a subscription expiration date.</span></span>
<span data-ttu-id="cbf0e-117">O valor padrão desse parâmetro é $Null.</span><span class="sxs-lookup"><span data-stu-id="cbf0e-117">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="cbf0e-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="cbf0e-118">-Name</span></span>
<span data-ttu-id="cbf0e-119">Especifica um nome de assinatura.</span><span class="sxs-lookup"><span data-stu-id="cbf0e-119">Specifies a subscription name.</span></span>

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

### <span data-ttu-id="cbf0e-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cbf0e-120">-PassThru</span></span>
<span data-ttu-id="cbf0e-121">PassThru</span><span class="sxs-lookup"><span data-stu-id="cbf0e-121">passthru</span></span>

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

### <span data-ttu-id="cbf0e-122">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="cbf0e-122">-PrimaryKey</span></span>
<span data-ttu-id="cbf0e-123">Especifica a chave primária de assinatura.</span><span class="sxs-lookup"><span data-stu-id="cbf0e-123">Specifies the subscription primary key.</span></span>
<span data-ttu-id="cbf0e-124">Esse parâmetro é gerado automaticamente se não for especificado.</span><span class="sxs-lookup"><span data-stu-id="cbf0e-124">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="cbf0e-125">Esse parâmetro deve ter de 1 a 300 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="cbf0e-125">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="cbf0e-126">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="cbf0e-126">-SecondaryKey</span></span>
<span data-ttu-id="cbf0e-127">Especifica a chave secundária de assinatura.</span><span class="sxs-lookup"><span data-stu-id="cbf0e-127">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="cbf0e-128">Esse parâmetro é gerado automaticamente se não for especificado.</span><span class="sxs-lookup"><span data-stu-id="cbf0e-128">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="cbf0e-129">Esse parâmetro deve ter de 1 a 300 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="cbf0e-129">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="cbf0e-130">-Estado</span><span class="sxs-lookup"><span data-stu-id="cbf0e-130">-State</span></span>
<span data-ttu-id="cbf0e-131">Especifica o estado da assinatura.</span><span class="sxs-lookup"><span data-stu-id="cbf0e-131">Specifies the subscription state.</span></span>
<span data-ttu-id="cbf0e-132">O valor padrão desse parâmetro é $Null.</span><span class="sxs-lookup"><span data-stu-id="cbf0e-132">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="cbf0e-133">-StateComment</span><span class="sxs-lookup"><span data-stu-id="cbf0e-133">-StateComment</span></span>
<span data-ttu-id="cbf0e-134">Especifica o comentário do estado da assinatura.</span><span class="sxs-lookup"><span data-stu-id="cbf0e-134">Specifies the subscription state comment.</span></span>
<span data-ttu-id="cbf0e-135">O valor padrão desse parâmetro é $Null.</span><span class="sxs-lookup"><span data-stu-id="cbf0e-135">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="cbf0e-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cbf0e-136">-SubscriptionId</span></span>
<span data-ttu-id="cbf0e-137">Especifica a ID da assinatura.</span><span class="sxs-lookup"><span data-stu-id="cbf0e-137">Specifies the subscription ID.</span></span>

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

### <span data-ttu-id="cbf0e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbf0e-138">CommonParameters</span></span>
<span data-ttu-id="cbf0e-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbf0e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbf0e-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cbf0e-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbf0e-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cbf0e-141">INPUTS</span></span>

### <span data-ttu-id="cbf0e-142">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="cbf0e-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="cbf0e-143">System. String</span><span class="sxs-lookup"><span data-stu-id="cbf0e-143">System.String</span></span>

### <span data-ttu-id="cbf0e-144">System. Nullable ' 1 [[Microsoft. Azure. Commands. ApiManagement. Management. Models. PsApiManagementSubscriptionState, Microsoft. Azure. PowerShell. cmdlets. ApiManagement. immanagement, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="cbf0e-144">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="cbf0e-145">System. Nullable ' 1 [[System. DateTime, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="cbf0e-145">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="cbf0e-146">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="cbf0e-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="cbf0e-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cbf0e-147">OUTPUTS</span></span>

### <span data-ttu-id="cbf0e-148">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="cbf0e-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="cbf0e-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cbf0e-149">NOTES</span></span>

## <span data-ttu-id="cbf0e-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cbf0e-150">RELATED LINKS</span></span>

[<span data-ttu-id="cbf0e-151">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="cbf0e-151">Get-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="cbf0e-152">New-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="cbf0e-152">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="cbf0e-153">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="cbf0e-153">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)


