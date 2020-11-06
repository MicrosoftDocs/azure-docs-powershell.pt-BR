---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 3B5FC8E3-5A02-4F3B-81F0-51DFE47A201B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementTenantAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementTenantAccess.md
ms.openlocfilehash: c75aceee59e5696d928f19fa6d5ae317828fa82f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427015"
---
# <span data-ttu-id="9b2c6-101">Set-AzureRmApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="9b2c6-101">Set-AzureRmApiManagementTenantAccess</span></span>

## <span data-ttu-id="9b2c6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9b2c6-102">SYNOPSIS</span></span>
<span data-ttu-id="9b2c6-103">Habilita ou desabilita o acesso do locatário.</span><span class="sxs-lookup"><span data-stu-id="9b2c6-103">Enables or disables tenant access.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9b2c6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9b2c6-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementTenantAccess -Context <PsApiManagementContext> -Enabled <Boolean> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9b2c6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9b2c6-105">DESCRIPTION</span></span>
<span data-ttu-id="9b2c6-106">O cmdlet **set-AzureRmApiManagementTenantAccess** habilita ou desabilita o acesso do locatário.</span><span class="sxs-lookup"><span data-stu-id="9b2c6-106">The **Set-AzureRmApiManagementTenantAccess** cmdlet enables or disables tenant access.</span></span>

## <span data-ttu-id="9b2c6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9b2c6-107">EXAMPLES</span></span>

### <span data-ttu-id="9b2c6-108">Exemplo 1: habilitar o acesso ao locatário</span><span class="sxs-lookup"><span data-stu-id="9b2c6-108">Example 1: Enable tenant access</span></span>
```
PS C:\>Set-AzureRmApiManagementTenantAccess -Context $ApimContext -Enabled $True
```

<span data-ttu-id="9b2c6-109">Esse comando habilita o acesso do locatário no contexto especificado.</span><span class="sxs-lookup"><span data-stu-id="9b2c6-109">This command enables tenant access in the specified context.</span></span>

## <span data-ttu-id="9b2c6-110">OS</span><span class="sxs-lookup"><span data-stu-id="9b2c6-110">PARAMETERS</span></span>

### <span data-ttu-id="9b2c6-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="9b2c6-111">-Context</span></span>
<span data-ttu-id="9b2c6-112">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="9b2c6-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="9b2c6-113">Habilitado para o</span><span class="sxs-lookup"><span data-stu-id="9b2c6-113">-Enabled</span></span>
<span data-ttu-id="9b2c6-114">Especifica se esse cmdlet habilita ou desabilita o acesso ao locatário.</span><span class="sxs-lookup"><span data-stu-id="9b2c6-114">Specifies whether this cmdlet enables or disables tenant access.</span></span>
<span data-ttu-id="9b2c6-115">Especifique um valor de $True para habilitar ou $False para desabilitar.</span><span class="sxs-lookup"><span data-stu-id="9b2c6-115">Specify a value of $True to enable or $False to disable.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b2c6-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9b2c6-116">-PassThru</span></span>
<span data-ttu-id="9b2c6-117">Indica que esse cmdlet retorna o **PsApiManagementAccessInformation** que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="9b2c6-117">Indicates that this cmdlet returns the **PsApiManagementAccessInformation** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="9b2c6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b2c6-118">-DefaultProfile</span></span>
<span data-ttu-id="9b2c6-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9b2c6-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b2c6-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b2c6-120">CommonParameters</span></span>
<span data-ttu-id="9b2c6-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b2c6-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b2c6-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b2c6-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b2c6-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9b2c6-123">INPUTS</span></span>

## <span data-ttu-id="9b2c6-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9b2c6-124">OUTPUTS</span></span>

### <span data-ttu-id="9b2c6-125">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="9b2c6-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="9b2c6-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9b2c6-126">NOTES</span></span>

## <span data-ttu-id="9b2c6-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9b2c6-127">RELATED LINKS</span></span>

[<span data-ttu-id="9b2c6-128">Get-AzureRmApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="9b2c6-128">Get-AzureRmApiManagementTenantAccess</span></span>](./Get-AzureRmApiManagementTenantAccess.md)


