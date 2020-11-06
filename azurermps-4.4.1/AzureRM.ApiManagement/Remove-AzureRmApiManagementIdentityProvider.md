---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementIdentityProvider.md
ms.openlocfilehash: ecbb2b6671f1482f31cb7b3f0b07d4e9be4bbb3a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428317"
---
# <span data-ttu-id="d15bb-101">Remove-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="d15bb-101">Remove-AzureRmApiManagementIdentityProvider</span></span>

## <span data-ttu-id="d15bb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d15bb-102">SYNOPSIS</span></span>
<span data-ttu-id="d15bb-103">Remove uma configuração de provedor de identidade existente.</span><span class="sxs-lookup"><span data-stu-id="d15bb-103">Removes an existing Identity Provider Configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d15bb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d15bb-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d15bb-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d15bb-105">DESCRIPTION</span></span>
<span data-ttu-id="d15bb-106">Remove uma configuração de provedor de identidade existente.</span><span class="sxs-lookup"><span data-stu-id="d15bb-106">Removes an existing Identity Provider Configuration.</span></span>

## <span data-ttu-id="d15bb-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d15bb-107">EXAMPLES</span></span>

### <span data-ttu-id="d15bb-108">Remove as configurações do provedor de identidade do Facebook do serviço ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d15bb-108">Removes the Facebook identity provider settings from ApiManagement service</span></span>
```
Remove-AzureRmApiManagementIdentityProvider -Context $apimContext -Type 'Facebook' -PassThru
```

<span data-ttu-id="d15bb-109">Exclui a configuração relacionada à configuração do provedor de identidade do Facebook.</span><span class="sxs-lookup"><span data-stu-id="d15bb-109">Deletes configuration related to Facebook Identity provider configuration.</span></span>

## <span data-ttu-id="d15bb-110">OS</span><span class="sxs-lookup"><span data-stu-id="d15bb-110">PARAMETERS</span></span>

### <span data-ttu-id="d15bb-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="d15bb-111">-Context</span></span>
<span data-ttu-id="d15bb-112">Instância do PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="d15bb-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="d15bb-113">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="d15bb-113">This parameter is required.</span></span>

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

### <span data-ttu-id="d15bb-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d15bb-114">-PassThru</span></span>
<span data-ttu-id="d15bb-115">Indica que esse cmdlet retorna um valor de $True se a operação for bem-sucedida ou $False caso contrário.</span><span class="sxs-lookup"><span data-stu-id="d15bb-115">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>


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

### <span data-ttu-id="d15bb-116">-Digite</span><span class="sxs-lookup"><span data-stu-id="d15bb-116">-Type</span></span>
<span data-ttu-id="d15bb-117">Identificador de um provedor de identidade existente.</span><span class="sxs-lookup"><span data-stu-id="d15bb-117">Identifier of an existing Identity Provider.</span></span>
<span data-ttu-id="d15bb-118">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="d15bb-118">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType
Parameter Sets: (All)
Aliases: 
Accepted values: Facebook, Google, Microsoft, Twitter, Aad

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d15bb-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d15bb-119">-Confirm</span></span>
<span data-ttu-id="d15bb-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d15bb-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d15bb-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d15bb-121">-WhatIf</span></span>
<span data-ttu-id="d15bb-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d15bb-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d15bb-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d15bb-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d15bb-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d15bb-124">-DefaultProfile</span></span>
<span data-ttu-id="d15bb-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d15bb-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d15bb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d15bb-126">CommonParameters</span></span>
<span data-ttu-id="d15bb-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d15bb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d15bb-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d15bb-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d15bb-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d15bb-129">INPUTS</span></span>

## <span data-ttu-id="d15bb-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d15bb-130">OUTPUTS</span></span>

### <span data-ttu-id="d15bb-131">bool</span><span class="sxs-lookup"><span data-stu-id="d15bb-131">bool</span></span>

## <span data-ttu-id="d15bb-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d15bb-132">NOTES</span></span>

## <span data-ttu-id="d15bb-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d15bb-133">RELATED LINKS</span></span>

[<span data-ttu-id="d15bb-134">New-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="d15bb-134">New-AzureRmApiManagementIdentityProvider</span></span>](./New-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="d15bb-135">Get-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="d15bb-135">Get-AzureRmApiManagementIdentityProvider</span></span>](./Get-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="d15bb-136">Set-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="d15bb-136">Set-AzureRmApiManagementIdentityProvider</span></span>](./Set-AzureRmApiManagementIdentityProvider.md)

