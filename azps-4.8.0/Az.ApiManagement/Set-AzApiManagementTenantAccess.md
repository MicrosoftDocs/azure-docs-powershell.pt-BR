---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 3B5FC8E3-5A02-4F3B-81F0-51DFE47A201B
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementtenantaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementTenantAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementTenantAccess.md
ms.openlocfilehash: 08bbb81998107a11a5996cb75a6fba8b760802db
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94112661"
---
# <span data-ttu-id="36241-101">Set-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="36241-101">Set-AzApiManagementTenantAccess</span></span>

## <span data-ttu-id="36241-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="36241-102">SYNOPSIS</span></span>
<span data-ttu-id="36241-103">Habilita ou desabilita o acesso do locatário.</span><span class="sxs-lookup"><span data-stu-id="36241-103">Enables or disables tenant access.</span></span>

## <span data-ttu-id="36241-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="36241-104">SYNTAX</span></span>

```
Set-AzApiManagementTenantAccess -Context <PsApiManagementContext> -Enabled <Boolean> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="36241-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="36241-105">DESCRIPTION</span></span>
<span data-ttu-id="36241-106">O cmdlet **set-AzApiManagementTenantAccess** habilita ou desabilita o acesso do locatário.</span><span class="sxs-lookup"><span data-stu-id="36241-106">The **Set-AzApiManagementTenantAccess** cmdlet enables or disables tenant access.</span></span>

## <span data-ttu-id="36241-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="36241-107">EXAMPLES</span></span>

### <span data-ttu-id="36241-108">Exemplo 1: habilitar o acesso ao locatário</span><span class="sxs-lookup"><span data-stu-id="36241-108">Example 1: Enable tenant access</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementTenantAccess -Context $apimContext -Enabled $True
```

<span data-ttu-id="36241-109">Esse comando habilita o acesso do locatário no contexto especificado.</span><span class="sxs-lookup"><span data-stu-id="36241-109">This command enables tenant access in the specified context.</span></span>

## <span data-ttu-id="36241-110">OS</span><span class="sxs-lookup"><span data-stu-id="36241-110">PARAMETERS</span></span>

### <span data-ttu-id="36241-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="36241-111">-Context</span></span>
<span data-ttu-id="36241-112">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="36241-112">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="36241-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36241-113">-DefaultProfile</span></span>
<span data-ttu-id="36241-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="36241-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="36241-115">Habilitado para o</span><span class="sxs-lookup"><span data-stu-id="36241-115">-Enabled</span></span>
<span data-ttu-id="36241-116">Especifica se esse cmdlet habilita ou desabilita o acesso ao locatário.</span><span class="sxs-lookup"><span data-stu-id="36241-116">Specifies whether this cmdlet enables or disables tenant access.</span></span>
<span data-ttu-id="36241-117">Especifique um valor de $True para habilitar ou $False para desabilitar.</span><span class="sxs-lookup"><span data-stu-id="36241-117">Specify a value of $True to enable or $False to disable.</span></span>

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

### <span data-ttu-id="36241-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="36241-118">-PassThru</span></span>
<span data-ttu-id="36241-119">Indica que esse cmdlet retorna o **PsApiManagementAccessInformation** que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="36241-119">Indicates that this cmdlet returns the **PsApiManagementAccessInformation** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="36241-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36241-120">CommonParameters</span></span>
<span data-ttu-id="36241-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36241-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36241-122">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="36241-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36241-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="36241-123">INPUTS</span></span>

### <span data-ttu-id="36241-124">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="36241-124">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="36241-125">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="36241-125">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="36241-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="36241-126">OUTPUTS</span></span>

### <span data-ttu-id="36241-127">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="36241-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="36241-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="36241-128">NOTES</span></span>

## <span data-ttu-id="36241-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="36241-129">RELATED LINKS</span></span>

[<span data-ttu-id="36241-130">Get-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="36241-130">Get-AzApiManagementTenantAccess</span></span>](./Get-AzApiManagementTenantAccess.md)


