---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 52115C49-0229-4F2C-B7B0-02FC52C1D32D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementSubscription.md
ms.openlocfilehash: 3b6d07577a6df05a57ed7675f5d14c847e8c33fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428014"
---
# <span data-ttu-id="5f5ae-101">Set-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="5f5ae-101">Set-AzureRmApiManagementSubscription</span></span>

## <span data-ttu-id="5f5ae-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5f5ae-102">SYNOPSIS</span></span>
<span data-ttu-id="5f5ae-103">Define detalhes de assinatura existentes.</span><span class="sxs-lookup"><span data-stu-id="5f5ae-103">Sets existing subscription details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5f5ae-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5f5ae-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String>
 [-Name <String>] [-PrimaryKey <String>] [-SecondaryKey <String>] [-State <PsApiManagementSubscriptionState>]
 [-ExpiresOn <DateTime>] [-StateComment <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5f5ae-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5f5ae-105">DESCRIPTION</span></span>
<span data-ttu-id="5f5ae-106">O cmdlet **set-AzureRmApiManagementSubscription** define os detalhes da assinatura existente.</span><span class="sxs-lookup"><span data-stu-id="5f5ae-106">The **Set-AzureRmApiManagementSubscription** cmdlet sets existing subscription details.</span></span>

## <span data-ttu-id="5f5ae-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5f5ae-107">EXAMPLES</span></span>

### <span data-ttu-id="5f5ae-108">Exemplo 1: definir o estado e as chaves primárias e secundárias para uma assinatura</span><span class="sxs-lookup"><span data-stu-id="5f5ae-108">Example 1: Set the state and primary and secondary keys for a subscription</span></span>
```
PS C:\>Set-AzureRmApiManagementSubscription -Context $apimContext -SubscriptionId -0123456789 -PrimaryKey "80450f7d0b6d481382113073f67822c1" -SencondaryKey "97d6112c3a8f48d5bf0266b7a09a761c" -State "Active"
```

<span data-ttu-id="5f5ae-109">Este comando define as chaves primária e secundária para uma assinatura e a ativa.</span><span class="sxs-lookup"><span data-stu-id="5f5ae-109">This command sets the primary and secondary keys for a subscription and activates it.</span></span>

## <span data-ttu-id="5f5ae-110">OS</span><span class="sxs-lookup"><span data-stu-id="5f5ae-110">PARAMETERS</span></span>

### <span data-ttu-id="5f5ae-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="5f5ae-111">-Context</span></span>
<span data-ttu-id="5f5ae-112">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="5f5ae-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="5f5ae-113">-ExpiresOn</span><span class="sxs-lookup"><span data-stu-id="5f5ae-113">-ExpiresOn</span></span>
<span data-ttu-id="5f5ae-114">Especifica uma data de validade da assinatura.</span><span class="sxs-lookup"><span data-stu-id="5f5ae-114">Specifies a subscription expiration date.</span></span>
<span data-ttu-id="5f5ae-115">O valor padrão desse parâmetro é $Null.</span><span class="sxs-lookup"><span data-stu-id="5f5ae-115">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="5f5ae-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="5f5ae-116">-Name</span></span>
<span data-ttu-id="5f5ae-117">Especifica um nome de assinatura.</span><span class="sxs-lookup"><span data-stu-id="5f5ae-117">Specifies a subscription name.</span></span>

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

### <span data-ttu-id="5f5ae-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5f5ae-118">-PassThru</span></span>
<span data-ttu-id="5f5ae-119">PassThru</span><span class="sxs-lookup"><span data-stu-id="5f5ae-119">passthru</span></span>

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

### <span data-ttu-id="5f5ae-120">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="5f5ae-120">-PrimaryKey</span></span>
<span data-ttu-id="5f5ae-121">Especifica a chave primária de assinatura.</span><span class="sxs-lookup"><span data-stu-id="5f5ae-121">Specifies the subscription primary key.</span></span>
<span data-ttu-id="5f5ae-122">Esse parâmetro é gerado automaticamente se não for especificado.</span><span class="sxs-lookup"><span data-stu-id="5f5ae-122">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="5f5ae-123">Esse parâmetro deve ter de 1 a 300 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="5f5ae-123">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="5f5ae-124">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="5f5ae-124">-SecondaryKey</span></span>
<span data-ttu-id="5f5ae-125">Especifica a chave secundária de assinatura.</span><span class="sxs-lookup"><span data-stu-id="5f5ae-125">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="5f5ae-126">Esse parâmetro é gerado automaticamente se não for especificado.</span><span class="sxs-lookup"><span data-stu-id="5f5ae-126">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="5f5ae-127">Esse parâmetro deve ter de 1 a 300 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="5f5ae-127">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="5f5ae-128">-Estado</span><span class="sxs-lookup"><span data-stu-id="5f5ae-128">-State</span></span>
<span data-ttu-id="5f5ae-129">Especifica o estado da assinatura.</span><span class="sxs-lookup"><span data-stu-id="5f5ae-129">Specifies the subscription state.</span></span>
<span data-ttu-id="5f5ae-130">O valor padrão desse parâmetro é $Null.</span><span class="sxs-lookup"><span data-stu-id="5f5ae-130">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="5f5ae-131">-StateComment</span><span class="sxs-lookup"><span data-stu-id="5f5ae-131">-StateComment</span></span>
<span data-ttu-id="5f5ae-132">Especifica o comentário do estado da assinatura.</span><span class="sxs-lookup"><span data-stu-id="5f5ae-132">Specifies the subscription state comment.</span></span>
<span data-ttu-id="5f5ae-133">O valor padrão desse parâmetro é $Null.</span><span class="sxs-lookup"><span data-stu-id="5f5ae-133">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="5f5ae-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5f5ae-134">-SubscriptionId</span></span>
<span data-ttu-id="5f5ae-135">Especifica a ID da assinatura.</span><span class="sxs-lookup"><span data-stu-id="5f5ae-135">Specifies the subscription ID.</span></span>

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

### <span data-ttu-id="5f5ae-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f5ae-136">-DefaultProfile</span></span>
<span data-ttu-id="5f5ae-137">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5f5ae-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5f5ae-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f5ae-138">CommonParameters</span></span>
<span data-ttu-id="5f5ae-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f5ae-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f5ae-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f5ae-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f5ae-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5f5ae-141">INPUTS</span></span>

## <span data-ttu-id="5f5ae-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5f5ae-142">OUTPUTS</span></span>

### <span data-ttu-id="5f5ae-143">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementSubscripition</span><span class="sxs-lookup"><span data-stu-id="5f5ae-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscripition</span></span>

## <span data-ttu-id="5f5ae-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5f5ae-144">NOTES</span></span>

## <span data-ttu-id="5f5ae-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5f5ae-145">RELATED LINKS</span></span>

[<span data-ttu-id="5f5ae-146">Get-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="5f5ae-146">Get-AzureRmApiManagementSubscription</span></span>](./Get-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="5f5ae-147">New-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="5f5ae-147">New-AzureRmApiManagementSubscription</span></span>](./New-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="5f5ae-148">Remove-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="5f5ae-148">Remove-AzureRmApiManagementSubscription</span></span>](./Remove-AzureRmApiManagementSubscription.md)


