---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: EE3D2BA0-32E7-4A37-BCAF-F0E8FAAC43CE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSSLBinding.md
ms.openlocfilehash: ae97bc08e5ba8c801e3bf5126c6e48dfb7910751
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426250"
---
# <span data-ttu-id="d7eb4-101">Get-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="d7eb4-101">Get-AzureRmWebAppSSLBinding</span></span>

## <span data-ttu-id="d7eb4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d7eb4-102">SYNOPSIS</span></span>
<span data-ttu-id="d7eb4-103">Obtém uma associação SSL do certificado do aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="d7eb4-103">Gets an Azure Web App certificate SSL binding.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7eb4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d7eb4-104">SYNTAX</span></span>

### <span data-ttu-id="d7eb4-105">Eles</span><span class="sxs-lookup"><span data-stu-id="d7eb4-105">S1</span></span>
```
Get-AzureRmWebAppSSLBinding [[-Name] <String>] [-ResourceGroupName] <String> [-WebAppName] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d7eb4-106">S2</span><span class="sxs-lookup"><span data-stu-id="d7eb4-106">S2</span></span>
```
Get-AzureRmWebAppSSLBinding [[-Name] <String>] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d7eb4-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d7eb4-107">DESCRIPTION</span></span>
<span data-ttu-id="d7eb4-108">O cmdlet **Get-AzureRmWebAppSSLBinding** Obtém uma associação SSL (Secure Sockets Layer) para um aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="d7eb4-108">The **Get-AzureRmWebAppSSLBinding** cmdlet gets a Secure Sockets Layer (SSL) binding for an Azure Web App.</span></span>
<span data-ttu-id="d7eb4-109">Associações SSL são usadas para associar um aplicativo Web a um certificado carregado.</span><span class="sxs-lookup"><span data-stu-id="d7eb4-109">SSL bindings are used to associate a Web App with an uploaded certificate.</span></span>
<span data-ttu-id="d7eb4-110">Os aplicativos Web podem ser associados a vários certificados.</span><span class="sxs-lookup"><span data-stu-id="d7eb4-110">Web Apps can be bound to multiple certificates.</span></span>

## <span data-ttu-id="d7eb4-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d7eb4-111">EXAMPLES</span></span>

### <span data-ttu-id="d7eb4-112">Exemplo 1: obter associações SSL para um aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="d7eb4-112">Example 1: Get SSL bindings for a Web App</span></span>
```
PS C:\>Get-AzureRmWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp"
```

<span data-ttu-id="d7eb4-113">Esse comando recupera as associações SSL para o aplicativo Web ContosoWebApp, que está associado à ContosoResourceGroup do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d7eb4-113">This command retrieves the SSL bindings for the Web App ContosoWebApp, which is associated with the resource group ContosoResourceGroup.</span></span>

### <span data-ttu-id="d7eb4-114">Exemplo 2: usar uma referência de objeto para obter associações SSL para um aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="d7eb4-114">Example 2: Use an object reference to get SSL bindings for a Web App</span></span>
```
PS C:\>$WebApp = Get-AzureRmWebApp -Name "ContosoWebApp"
PS C:\> Get-AzureRmWebAppSSLBinding -WebApp $WebApp
```

<span data-ttu-id="d7eb4-115">Os comandos neste exemplo também obtêm associações SSL para o aplicativo Web ContosoWebApp; Nesse caso, no entanto, uma referência de objeto é usada em vez do nome do aplicativo Web e o nome do grupo de recursos associado.</span><span class="sxs-lookup"><span data-stu-id="d7eb4-115">The commands in this example also get the SSL bindings for the Web App ContosoWebApp; in this case, however, an object reference is used instead of the Web App name and the name of the associated resource group.</span></span>
<span data-ttu-id="d7eb4-116">Essa referência de objeto é criada pelo primeiro comando no exemplo, que usa **Get-AzureRmWebApp** para criar uma referência de objeto para o aplicativo Web chamado ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="d7eb4-116">This object reference is created by the first command in the example, which uses **Get-AzureRmWebApp** to create an object reference to the Web App named ContosoWebApp.</span></span>
<span data-ttu-id="d7eb4-117">Essa referência de objeto é armazenada em uma variável chamada $WebApp.</span><span class="sxs-lookup"><span data-stu-id="d7eb4-117">That object reference is stored in a variable named $WebApp.</span></span>
<span data-ttu-id="d7eb4-118">Essa variável, e o cmdlet **Get-AzureRmWebAppSSLBinding** , são então usadas pelo segundo comando para obter as associações SSL.</span><span class="sxs-lookup"><span data-stu-id="d7eb4-118">This variable, and the **Get-AzureRmWebAppSSLBinding** cmdlet, are then used by the second command to get the SSL bindings.</span></span>

## <span data-ttu-id="d7eb4-119">OS</span><span class="sxs-lookup"><span data-stu-id="d7eb4-119">PARAMETERS</span></span>

### <span data-ttu-id="d7eb4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7eb4-120">-DefaultProfile</span></span>
<span data-ttu-id="d7eb4-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d7eb4-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d7eb4-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="d7eb4-122">-Name</span></span>
<span data-ttu-id="d7eb4-123">Especifica o nome da Associação SSL.</span><span class="sxs-lookup"><span data-stu-id="d7eb4-123">Specifies the name of the SSL binding.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7eb4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7eb4-124">-ResourceGroupName</span></span>
<span data-ttu-id="d7eb4-125">Especifica o nome do grupo de recursos ao qual o certificado está atribuído.</span><span class="sxs-lookup"><span data-stu-id="d7eb4-125">Specifies the name of the resource group that the certificate is assigned to.</span></span>
<span data-ttu-id="d7eb4-126">Não é possível usar o parâmetro *ResourceGroupName* e o parâmetro *webapp* no mesmo comando.</span><span class="sxs-lookup"><span data-stu-id="d7eb4-126">You cannot use the *ResourceGroupName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7eb4-127">-Slot</span><span class="sxs-lookup"><span data-stu-id="d7eb4-127">-Slot</span></span>
<span data-ttu-id="d7eb4-128">Especifica um slot de implantação do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="d7eb4-128">Specifies a Web App deployment slot.</span></span>
<span data-ttu-id="d7eb4-129">Para obter um slot de implantação, use o cmdlet Get-AzureRMWebAppSlot.</span><span class="sxs-lookup"><span data-stu-id="d7eb4-129">To get a deployment slot, use the Get-AzureRMWebAppSlot cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7eb4-130">-WebApp</span><span class="sxs-lookup"><span data-stu-id="d7eb4-130">-WebApp</span></span>
<span data-ttu-id="d7eb4-131">Especifica um aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="d7eb4-131">Specifies a Web App.</span></span>
<span data-ttu-id="d7eb4-132">Para obter um aplicativo Web, use o cmdlet Get-AzureRmWebApp.</span><span class="sxs-lookup"><span data-stu-id="d7eb4-132">To get a Web App, use the Get-AzureRmWebApp cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d7eb4-133">-WebAppname</span><span class="sxs-lookup"><span data-stu-id="d7eb4-133">-WebAppName</span></span>
<span data-ttu-id="d7eb4-134">Especifica o nome do aplicativo Web do qual este cmdlet obtém associações SSL.</span><span class="sxs-lookup"><span data-stu-id="d7eb4-134">Specifies the name of the Web App that this cmdlet gets SSL bindings from.</span></span>
<span data-ttu-id="d7eb4-135">Não é possível usar o parâmetro *webappname* e o parâmetro *webapp* no mesmo comando.</span><span class="sxs-lookup"><span data-stu-id="d7eb4-135">You cannot use the *WebAppName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7eb4-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7eb4-136">CommonParameters</span></span>
<span data-ttu-id="d7eb4-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7eb4-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7eb4-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7eb4-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7eb4-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d7eb4-139">INPUTS</span></span>

### <span data-ttu-id="d7eb4-140">Microsoft. Azure. Management. WebSites. Models. site</span><span class="sxs-lookup"><span data-stu-id="d7eb4-140">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="d7eb4-141">Parâmetros: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d7eb4-141">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="d7eb4-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d7eb4-142">OUTPUTS</span></span>

### <span data-ttu-id="d7eb4-143">Microsoft. Azure. Management. WebSites. Models. HostNameSslState</span><span class="sxs-lookup"><span data-stu-id="d7eb4-143">Microsoft.Azure.Management.WebSites.Models.HostNameSslState</span></span>

## <span data-ttu-id="d7eb4-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d7eb4-144">NOTES</span></span>

## <span data-ttu-id="d7eb4-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d7eb4-145">RELATED LINKS</span></span>

[<span data-ttu-id="d7eb4-146">New-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="d7eb4-146">New-AzureRmWebAppSSLBinding</span></span>](./New-AzureRmWebAppSSLBinding.md)

[<span data-ttu-id="d7eb4-147">Remove-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="d7eb4-147">Remove-AzureRmWebAppSSLBinding</span></span>](./Remove-AzureRmWebAppSSLBinding.md)

[<span data-ttu-id="d7eb4-148">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="d7eb4-148">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)


