---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementIdentityProvider.md
ms.openlocfilehash: 92e241703723d055d18083daae5fe424933f7c3b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440532"
---
# <span data-ttu-id="e0b72-101">Remove-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="e0b72-101">Remove-AzureRmApiManagementIdentityProvider</span></span>

## <span data-ttu-id="e0b72-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e0b72-102">SYNOPSIS</span></span>
<span data-ttu-id="e0b72-103">Remove uma configuração de provedor de identidade existente.</span><span class="sxs-lookup"><span data-stu-id="e0b72-103">Removes an existing Identity Provider Configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e0b72-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e0b72-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0b72-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e0b72-105">DESCRIPTION</span></span>
<span data-ttu-id="e0b72-106">Remove uma configuração de provedor de identidade existente.</span><span class="sxs-lookup"><span data-stu-id="e0b72-106">Removes an existing Identity Provider Configuration.</span></span>

## <span data-ttu-id="e0b72-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e0b72-107">EXAMPLES</span></span>

### <span data-ttu-id="e0b72-108">Remove as configurações do provedor de identidade do Facebook do serviço ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e0b72-108">Removes the Facebook identity provider settings from ApiManagement service</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementIdentityProvider -Context $apimContext -Type 'Facebook' -PassThru
```

<span data-ttu-id="e0b72-109">Exclui a configuração relacionada à configuração do provedor de identidade do Facebook.</span><span class="sxs-lookup"><span data-stu-id="e0b72-109">Deletes configuration related to Facebook Identity provider configuration.</span></span>

## <span data-ttu-id="e0b72-110">OS</span><span class="sxs-lookup"><span data-stu-id="e0b72-110">PARAMETERS</span></span>

### <span data-ttu-id="e0b72-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="e0b72-111">-Context</span></span>
<span data-ttu-id="e0b72-112">Instância do PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="e0b72-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="e0b72-113">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="e0b72-113">This parameter is required.</span></span>

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

### <span data-ttu-id="e0b72-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0b72-114">-DefaultProfile</span></span>
<span data-ttu-id="e0b72-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e0b72-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="e0b72-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e0b72-116">-PassThru</span></span>
<span data-ttu-id="e0b72-117">Indica que esse cmdlet retorna um valor de $True se a operação for bem-sucedida ou $False caso contrário.</span><span class="sxs-lookup"><span data-stu-id="e0b72-117">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>


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

### <span data-ttu-id="e0b72-118">-Digite</span><span class="sxs-lookup"><span data-stu-id="e0b72-118">-Type</span></span>
<span data-ttu-id="e0b72-119">Identificador de um provedor de identidade existente.</span><span class="sxs-lookup"><span data-stu-id="e0b72-119">Identifier of an existing Identity Provider.</span></span>
<span data-ttu-id="e0b72-120">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="e0b72-120">This parameter is required.</span></span>

```yaml
Type: PsApiManagementIdentityProviderType
Parameter Sets: (All)
Aliases: 
Accepted values: Facebook, Google, Microsoft, Twitter, Aad

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0b72-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e0b72-121">-Confirm</span></span>
<span data-ttu-id="e0b72-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0b72-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0b72-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0b72-123">-WhatIf</span></span>
<span data-ttu-id="e0b72-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e0b72-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e0b72-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e0b72-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0b72-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0b72-126">CommonParameters</span></span>
<span data-ttu-id="e0b72-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0b72-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0b72-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0b72-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0b72-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e0b72-129">INPUTS</span></span>

### <span data-ttu-id="e0b72-130">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="e0b72-130">None</span></span>
<span data-ttu-id="e0b72-131">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="e0b72-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e0b72-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e0b72-132">OUTPUTS</span></span>

### <span data-ttu-id="e0b72-133">bool</span><span class="sxs-lookup"><span data-stu-id="e0b72-133">bool</span></span>

## <span data-ttu-id="e0b72-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e0b72-134">NOTES</span></span>

## <span data-ttu-id="e0b72-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e0b72-135">RELATED LINKS</span></span>

[<span data-ttu-id="e0b72-136">New-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="e0b72-136">New-AzureRmApiManagementIdentityProvider</span></span>](./New-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="e0b72-137">Get-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="e0b72-137">Get-AzureRmApiManagementIdentityProvider</span></span>](./Get-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="e0b72-138">Set-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="e0b72-138">Set-AzureRmApiManagementIdentityProvider</span></span>](./Set-AzureRmApiManagementIdentityProvider.md)

