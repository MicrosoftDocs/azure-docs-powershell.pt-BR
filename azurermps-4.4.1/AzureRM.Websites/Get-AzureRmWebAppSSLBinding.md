---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: EE3D2BA0-32E7-4A37-BCAF-F0E8FAAC43CE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSSLBinding.md
ms.openlocfilehash: ae03fd4dedf1e0e6de91bd036180379c2be2cabe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429013"
---
# <span data-ttu-id="f6456-101">Get-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="f6456-101">Get-AzureRmWebAppSSLBinding</span></span>

## <span data-ttu-id="f6456-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f6456-102">SYNOPSIS</span></span>
<span data-ttu-id="f6456-103">Obtém uma associação SSL do certificado do aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="f6456-103">Gets an Azure Web App certificate SSL binding.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f6456-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f6456-104">SYNTAX</span></span>

### <span data-ttu-id="f6456-105">Eles</span><span class="sxs-lookup"><span data-stu-id="f6456-105">S1</span></span>
```
Get-AzureRmWebAppSSLBinding [[-Name] <String>] [-ResourceGroupName] <String> [-WebAppName] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f6456-106">S2</span><span class="sxs-lookup"><span data-stu-id="f6456-106">S2</span></span>
```
Get-AzureRmWebAppSSLBinding [[-Name] <String>] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f6456-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f6456-107">DESCRIPTION</span></span>
<span data-ttu-id="f6456-108">O cmdlet **Get-AzureRmWebAppSSLBinding** Obtém uma associação SSL (Secure Sockets Layer) para um aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="f6456-108">The **Get-AzureRmWebAppSSLBinding** cmdlet gets a Secure Sockets Layer (SSL) binding for an Azure Web App.</span></span>
<span data-ttu-id="f6456-109">Associações SSL são usadas para associar um aplicativo Web a um certificado carregado.</span><span class="sxs-lookup"><span data-stu-id="f6456-109">SSL bindings are used to associate a Web App with an uploaded certificate.</span></span>
<span data-ttu-id="f6456-110">Os aplicativos Web podem ser associados a vários certificados.</span><span class="sxs-lookup"><span data-stu-id="f6456-110">Web Apps can be bound to multiple certificates.</span></span>

## <span data-ttu-id="f6456-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f6456-111">EXAMPLES</span></span>

### <span data-ttu-id="f6456-112">Exemplo 1: obter associações SSL para um aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="f6456-112">Example 1: Get SSL bindings for a Web App</span></span>
```
PS C:\>Get-AzureRmWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp"
```

<span data-ttu-id="f6456-113">Esse comando recupera as associações SSL para o aplicativo Web ContosoWebApp, que está associado à ContosoResourceGroup do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f6456-113">This command retrieves the SSL bindings for the Web App ContosoWebApp, which is associated with the resource group ContosoResourceGroup.</span></span>

### <span data-ttu-id="f6456-114">Exemplo 2: usar uma referência de objeto para obter associações SSL para um aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="f6456-114">Example 2: Use an object reference to get SSL bindings for a Web App</span></span>
```
PS C:\>$WebApp = Get-AzureRmWebApp -Name "ContosoWebApp"
PS C:\> Get-AzureRmWebAppSSLBinding -WebApp $WebApp
```

<span data-ttu-id="f6456-115">Os comandos neste exemplo também obtêm associações SSL para o aplicativo Web ContosoWebApp; Nesse caso, no entanto, uma referência de objeto é usada em vez do nome do aplicativo Web e o nome do grupo de recursos associado.</span><span class="sxs-lookup"><span data-stu-id="f6456-115">The commands in this example also get the SSL bindings for the Web App ContosoWebApp; in this case, however, an object reference is used instead of the Web App name and the name of the associated resource group.</span></span>
<span data-ttu-id="f6456-116">Essa referência de objeto é criada pelo primeiro comando no exemplo, que usa **Get-AzureRmWebApp** para criar uma referência de objeto para o aplicativo Web chamado ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="f6456-116">This object reference is created by the first command in the example, which uses **Get-AzureRmWebApp** to create an object reference to the Web App named ContosoWebApp.</span></span>
<span data-ttu-id="f6456-117">Essa referência de objeto é armazenada em uma variável chamada $WebApp.</span><span class="sxs-lookup"><span data-stu-id="f6456-117">That object reference is stored in a variable named $WebApp.</span></span>

<span data-ttu-id="f6456-118">Essa variável, e o cmdlet **Get-AzureRmWebAppSSLBinding** , são então usadas pelo segundo comando para obter as associações SSL.</span><span class="sxs-lookup"><span data-stu-id="f6456-118">This variable, and the **Get-AzureRmWebAppSSLBinding** cmdlet, are then used by the second command to get the SSL bindings.</span></span>

## <span data-ttu-id="f6456-119">OS</span><span class="sxs-lookup"><span data-stu-id="f6456-119">PARAMETERS</span></span>

### <span data-ttu-id="f6456-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="f6456-120">-Name</span></span>
<span data-ttu-id="f6456-121">Especifica o nome da Associação SSL.</span><span class="sxs-lookup"><span data-stu-id="f6456-121">Specifies the name of the SSL binding.</span></span>

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

### <span data-ttu-id="f6456-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6456-122">-ResourceGroupName</span></span>
<span data-ttu-id="f6456-123">Especifica o nome do grupo de recursos ao qual o certificado está atribuído.</span><span class="sxs-lookup"><span data-stu-id="f6456-123">Specifies the name of the resource group that the certificate is assigned to.</span></span>

<span data-ttu-id="f6456-124">Não é possível usar o parâmetro *ResourceGroupName* e o parâmetro *webapp* no mesmo comando.</span><span class="sxs-lookup"><span data-stu-id="f6456-124">You cannot use the *ResourceGroupName* parameter and the *WebApp* parameter in the same command.</span></span>

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

### <span data-ttu-id="f6456-125">-Slot</span><span class="sxs-lookup"><span data-stu-id="f6456-125">-Slot</span></span>
<span data-ttu-id="f6456-126">Especifica um slot de implantação do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="f6456-126">Specifies a Web App deployment slot.</span></span>
<span data-ttu-id="f6456-127">Para obter um slot de implantação, use o cmdlet Get-AzureRMWebAppSlot.</span><span class="sxs-lookup"><span data-stu-id="f6456-127">To get a deployment slot, use the Get-AzureRMWebAppSlot cmdlet.</span></span>

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

### <span data-ttu-id="f6456-128">-WebApp</span><span class="sxs-lookup"><span data-stu-id="f6456-128">-WebApp</span></span>
<span data-ttu-id="f6456-129">Especifica um aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="f6456-129">Specifies a Web App.</span></span>
<span data-ttu-id="f6456-130">Para obter um aplicativo Web, use o cmdlet Get-AzureRmWebApp.</span><span class="sxs-lookup"><span data-stu-id="f6456-130">To get a Web App, use the Get-AzureRmWebApp cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f6456-131">-WebAppname</span><span class="sxs-lookup"><span data-stu-id="f6456-131">-WebAppName</span></span>
<span data-ttu-id="f6456-132">Especifica o nome do aplicativo Web do qual este cmdlet obtém associações SSL.</span><span class="sxs-lookup"><span data-stu-id="f6456-132">Specifies the name of the Web App that this cmdlet gets SSL bindings from.</span></span>

<span data-ttu-id="f6456-133">Não é possível usar o parâmetro *webappname* e o parâmetro *webapp* no mesmo comando.</span><span class="sxs-lookup"><span data-stu-id="f6456-133">You cannot use the *WebAppName* parameter and the *WebApp* parameter in the same command.</span></span>

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

### <span data-ttu-id="f6456-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6456-134">-DefaultProfile</span></span>
<span data-ttu-id="f6456-135">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f6456-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f6456-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6456-136">CommonParameters</span></span>
<span data-ttu-id="f6456-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6456-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6456-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6456-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6456-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f6456-139">INPUTS</span></span>

### <span data-ttu-id="f6456-140">Instalação</span><span class="sxs-lookup"><span data-stu-id="f6456-140">Site</span></span>
<span data-ttu-id="f6456-141">O parâmetro ' WebApp ' aceita o valor do tipo ' site ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="f6456-141">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="f6456-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f6456-142">OUTPUTS</span></span>

## <span data-ttu-id="f6456-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f6456-143">NOTES</span></span>

## <span data-ttu-id="f6456-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f6456-144">RELATED LINKS</span></span>

[<span data-ttu-id="f6456-145">New-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="f6456-145">New-AzureRmWebAppSSLBinding</span></span>](./New-AzureRmWebAppSSLBinding.md)

[<span data-ttu-id="f6456-146">Remove-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="f6456-146">Remove-AzureRmWebAppSSLBinding</span></span>](./Remove-AzureRmWebAppSSLBinding.md)

[<span data-ttu-id="f6456-147">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="f6456-147">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)


