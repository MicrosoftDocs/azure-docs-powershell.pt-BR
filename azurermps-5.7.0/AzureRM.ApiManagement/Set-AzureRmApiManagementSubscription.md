---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 52115C49-0229-4F2C-B7B0-02FC52C1D32D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementSubscription.md
ms.openlocfilehash: 62c1bd394dd509b81a8ea748c26c0465718926c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440143"
---
# <span data-ttu-id="270fb-101">Set-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="270fb-101">Set-AzureRmApiManagementSubscription</span></span>

## <span data-ttu-id="270fb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="270fb-102">SYNOPSIS</span></span>
<span data-ttu-id="270fb-103">Define detalhes de assinatura existentes.</span><span class="sxs-lookup"><span data-stu-id="270fb-103">Sets existing subscription details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="270fb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="270fb-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String>
 [-Name <String>] [-PrimaryKey <String>] [-SecondaryKey <String>] [-State <PsApiManagementSubscriptionState>]
 [-ExpiresOn <DateTime>] [-StateComment <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="270fb-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="270fb-105">DESCRIPTION</span></span>
<span data-ttu-id="270fb-106">O cmdlet **set-AzureRmApiManagementSubscription** define os detalhes da assinatura existente.</span><span class="sxs-lookup"><span data-stu-id="270fb-106">The **Set-AzureRmApiManagementSubscription** cmdlet sets existing subscription details.</span></span>

## <span data-ttu-id="270fb-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="270fb-107">EXAMPLES</span></span>

### <span data-ttu-id="270fb-108">Exemplo 1: definir o estado e as chaves primárias e secundárias para uma assinatura</span><span class="sxs-lookup"><span data-stu-id="270fb-108">Example 1: Set the state and primary and secondary keys for a subscription</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementSubscription -Context $apimContext -SubscriptionId -0123456789 -PrimaryKey "80450f7d0b6d481382113073f67822c1" -SecondaryKey "97d6112c3a8f48d5bf0266b7a09a761c" -State "Active"
```

<span data-ttu-id="270fb-109">Este comando define as chaves primária e secundária para uma assinatura e a ativa.</span><span class="sxs-lookup"><span data-stu-id="270fb-109">This command sets the primary and secondary keys for a subscription and activates it.</span></span>

## <span data-ttu-id="270fb-110">OS</span><span class="sxs-lookup"><span data-stu-id="270fb-110">PARAMETERS</span></span>

### <span data-ttu-id="270fb-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="270fb-111">-Context</span></span>
<span data-ttu-id="270fb-112">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="270fb-112">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="270fb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="270fb-113">-DefaultProfile</span></span>
<span data-ttu-id="270fb-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="270fb-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="270fb-115">-ExpiresOn</span><span class="sxs-lookup"><span data-stu-id="270fb-115">-ExpiresOn</span></span>
<span data-ttu-id="270fb-116">Especifica uma data de validade da assinatura.</span><span class="sxs-lookup"><span data-stu-id="270fb-116">Specifies a subscription expiration date.</span></span>
<span data-ttu-id="270fb-117">O valor padrão desse parâmetro é $Null.</span><span class="sxs-lookup"><span data-stu-id="270fb-117">The default value of this parameter is $Null.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="270fb-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="270fb-118">-Name</span></span>
<span data-ttu-id="270fb-119">Especifica um nome de assinatura.</span><span class="sxs-lookup"><span data-stu-id="270fb-119">Specifies a subscription name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="270fb-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="270fb-120">-PassThru</span></span>
<span data-ttu-id="270fb-121">PassThru</span><span class="sxs-lookup"><span data-stu-id="270fb-121">passthru</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="270fb-122">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="270fb-122">-PrimaryKey</span></span>
<span data-ttu-id="270fb-123">Especifica a chave primária de assinatura.</span><span class="sxs-lookup"><span data-stu-id="270fb-123">Specifies the subscription primary key.</span></span>
<span data-ttu-id="270fb-124">Esse parâmetro é gerado automaticamente se não for especificado.</span><span class="sxs-lookup"><span data-stu-id="270fb-124">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="270fb-125">Esse parâmetro deve ter de 1 a 300 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="270fb-125">This parameter must be 1 to 300 characters long.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="270fb-126">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="270fb-126">-SecondaryKey</span></span>
<span data-ttu-id="270fb-127">Especifica a chave secundária de assinatura.</span><span class="sxs-lookup"><span data-stu-id="270fb-127">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="270fb-128">Esse parâmetro é gerado automaticamente se não for especificado.</span><span class="sxs-lookup"><span data-stu-id="270fb-128">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="270fb-129">Esse parâmetro deve ter de 1 a 300 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="270fb-129">This parameter must be 1 to 300 characters long.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="270fb-130">-Estado</span><span class="sxs-lookup"><span data-stu-id="270fb-130">-State</span></span>
<span data-ttu-id="270fb-131">Especifica o estado da assinatura.</span><span class="sxs-lookup"><span data-stu-id="270fb-131">Specifies the subscription state.</span></span>
<span data-ttu-id="270fb-132">O valor padrão desse parâmetro é $Null.</span><span class="sxs-lookup"><span data-stu-id="270fb-132">The default value of this parameter is $Null.</span></span>

```yaml
Type: PsApiManagementSubscriptionState
Parameter Sets: (All)
Aliases: 
Accepted values: Suspended, Active, Expired, Submitted, Rejected, Cancelled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="270fb-133">-StateComment</span><span class="sxs-lookup"><span data-stu-id="270fb-133">-StateComment</span></span>
<span data-ttu-id="270fb-134">Especifica o comentário do estado da assinatura.</span><span class="sxs-lookup"><span data-stu-id="270fb-134">Specifies the subscription state comment.</span></span>
<span data-ttu-id="270fb-135">O valor padrão desse parâmetro é $Null.</span><span class="sxs-lookup"><span data-stu-id="270fb-135">The default value of this parameter is $Null.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="270fb-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="270fb-136">-SubscriptionId</span></span>
<span data-ttu-id="270fb-137">Especifica a ID da assinatura.</span><span class="sxs-lookup"><span data-stu-id="270fb-137">Specifies the subscription ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="270fb-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="270fb-138">CommonParameters</span></span>
<span data-ttu-id="270fb-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="270fb-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="270fb-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="270fb-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="270fb-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="270fb-141">INPUTS</span></span>

### <span data-ttu-id="270fb-142">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="270fb-142">None</span></span>
<span data-ttu-id="270fb-143">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="270fb-143">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="270fb-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="270fb-144">OUTPUTS</span></span>

### <span data-ttu-id="270fb-145">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementSubscripition</span><span class="sxs-lookup"><span data-stu-id="270fb-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscripition</span></span>

## <span data-ttu-id="270fb-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="270fb-146">NOTES</span></span>

## <span data-ttu-id="270fb-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="270fb-147">RELATED LINKS</span></span>

[<span data-ttu-id="270fb-148">Get-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="270fb-148">Get-AzureRmApiManagementSubscription</span></span>](./Get-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="270fb-149">New-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="270fb-149">New-AzureRmApiManagementSubscription</span></span>](./New-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="270fb-150">Remove-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="270fb-150">Remove-AzureRmApiManagementSubscription</span></span>](./Remove-AzureRmApiManagementSubscription.md)


