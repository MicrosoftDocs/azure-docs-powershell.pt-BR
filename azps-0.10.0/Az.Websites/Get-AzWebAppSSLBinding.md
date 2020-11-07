---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: EE3D2BA0-32E7-4A37-BCAF-F0E8FAAC43CE
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppSSLBinding.md
ms.openlocfilehash: 4c1739120c024629e68395f34a7f66b4259eb311
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776109"
---
# <span data-ttu-id="1c3b2-101">Get-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="1c3b2-101">Get-AzWebAppSSLBinding</span></span>

## <span data-ttu-id="1c3b2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1c3b2-102">SYNOPSIS</span></span>
<span data-ttu-id="1c3b2-103">Obtém uma associação SSL do certificado do aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="1c3b2-103">Gets an Azure Web App certificate SSL binding.</span></span>

## <span data-ttu-id="1c3b2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1c3b2-104">SYNTAX</span></span>

### <span data-ttu-id="1c3b2-105">Eles</span><span class="sxs-lookup"><span data-stu-id="1c3b2-105">S1</span></span>
```
Get-AzWebAppSSLBinding [[-Name] <String>] [-ResourceGroupName] <String> [-WebAppName] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1c3b2-106">S2</span><span class="sxs-lookup"><span data-stu-id="1c3b2-106">S2</span></span>
```
Get-AzWebAppSSLBinding [[-Name] <String>] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1c3b2-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1c3b2-107">DESCRIPTION</span></span>
<span data-ttu-id="1c3b2-108">O cmdlet **Get-AzWebAppSSLBinding** Obtém uma associação SSL (Secure Sockets Layer) para um aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="1c3b2-108">The **Get-AzWebAppSSLBinding** cmdlet gets a Secure Sockets Layer (SSL) binding for an Azure Web App.</span></span>
<span data-ttu-id="1c3b2-109">Associações SSL são usadas para associar um aplicativo Web a um certificado carregado.</span><span class="sxs-lookup"><span data-stu-id="1c3b2-109">SSL bindings are used to associate a Web App with an uploaded certificate.</span></span>
<span data-ttu-id="1c3b2-110">Os aplicativos Web podem ser associados a vários certificados.</span><span class="sxs-lookup"><span data-stu-id="1c3b2-110">Web Apps can be bound to multiple certificates.</span></span>

## <span data-ttu-id="1c3b2-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1c3b2-111">EXAMPLES</span></span>

### <span data-ttu-id="1c3b2-112">Exemplo 1: obter associações SSL para um aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="1c3b2-112">Example 1: Get SSL bindings for a Web App</span></span>
```
PS C:\>Get-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp"
```

<span data-ttu-id="1c3b2-113">Esse comando recupera as associações SSL para o aplicativo Web ContosoWebApp, que está associado à ContosoResourceGroup do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1c3b2-113">This command retrieves the SSL bindings for the Web App ContosoWebApp, which is associated with the resource group ContosoResourceGroup.</span></span>

### <span data-ttu-id="1c3b2-114">Exemplo 2: usar uma referência de objeto para obter associações SSL para um aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="1c3b2-114">Example 2: Use an object reference to get SSL bindings for a Web App</span></span>
```
PS C:\>$WebApp = Get-AzWebApp -Name "ContosoWebApp"
PS C:\> Get-AzWebAppSSLBinding -WebApp $WebApp
```

<span data-ttu-id="1c3b2-115">Os comandos neste exemplo também obtêm associações SSL para o aplicativo Web ContosoWebApp; Nesse caso, no entanto, uma referência de objeto é usada em vez do nome do aplicativo Web e o nome do grupo de recursos associado.</span><span class="sxs-lookup"><span data-stu-id="1c3b2-115">The commands in this example also get the SSL bindings for the Web App ContosoWebApp; in this case, however, an object reference is used instead of the Web App name and the name of the associated resource group.</span></span>
<span data-ttu-id="1c3b2-116">Essa referência de objeto é criada pelo primeiro comando no exemplo, que usa **Get-AzWebApp** para criar uma referência de objeto para o aplicativo Web chamado ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="1c3b2-116">This object reference is created by the first command in the example, which uses **Get-AzWebApp** to create an object reference to the Web App named ContosoWebApp.</span></span>
<span data-ttu-id="1c3b2-117">Essa referência de objeto é armazenada em uma variável chamada $WebApp.</span><span class="sxs-lookup"><span data-stu-id="1c3b2-117">That object reference is stored in a variable named $WebApp.</span></span>

<span data-ttu-id="1c3b2-118">Essa variável, e o cmdlet **Get-AzWebAppSSLBinding** , são então usadas pelo segundo comando para obter as associações SSL.</span><span class="sxs-lookup"><span data-stu-id="1c3b2-118">This variable, and the **Get-AzWebAppSSLBinding** cmdlet, are then used by the second command to get the SSL bindings.</span></span>

## <span data-ttu-id="1c3b2-119">OS</span><span class="sxs-lookup"><span data-stu-id="1c3b2-119">PARAMETERS</span></span>

### <span data-ttu-id="1c3b2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c3b2-120">-DefaultProfile</span></span>
<span data-ttu-id="1c3b2-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1c3b2-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c3b2-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="1c3b2-122">-Name</span></span>
<span data-ttu-id="1c3b2-123">Especifica o nome da Associação SSL.</span><span class="sxs-lookup"><span data-stu-id="1c3b2-123">Specifies the name of the SSL binding.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c3b2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c3b2-124">-ResourceGroupName</span></span>
<span data-ttu-id="1c3b2-125">Especifica o nome do grupo de recursos ao qual o certificado está atribuído.</span><span class="sxs-lookup"><span data-stu-id="1c3b2-125">Specifies the name of the resource group that the certificate is assigned to.</span></span>

<span data-ttu-id="1c3b2-126">Não é possível usar o parâmetro *ResourceGroupName* e o parâmetro *webapp* no mesmo comando.</span><span class="sxs-lookup"><span data-stu-id="1c3b2-126">You cannot use the *ResourceGroupName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c3b2-127">-Slot</span><span class="sxs-lookup"><span data-stu-id="1c3b2-127">-Slot</span></span>
<span data-ttu-id="1c3b2-128">Especifica um slot de implantação do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="1c3b2-128">Specifies a Web App deployment slot.</span></span>
<span data-ttu-id="1c3b2-129">Para obter um slot de implantação, use o cmdlet Get-AzWebAppSlot.</span><span class="sxs-lookup"><span data-stu-id="1c3b2-129">To get a deployment slot, use the Get-AzWebAppSlot cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c3b2-130">-WebApp</span><span class="sxs-lookup"><span data-stu-id="1c3b2-130">-WebApp</span></span>
<span data-ttu-id="1c3b2-131">Especifica um aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="1c3b2-131">Specifies a Web App.</span></span>
<span data-ttu-id="1c3b2-132">Para obter um aplicativo Web, use o cmdlet Get-AzWebApp.</span><span class="sxs-lookup"><span data-stu-id="1c3b2-132">To get a Web App, use the Get-AzWebApp cmdlet.</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1c3b2-133">-WebAppname</span><span class="sxs-lookup"><span data-stu-id="1c3b2-133">-WebAppName</span></span>
<span data-ttu-id="1c3b2-134">Especifica o nome do aplicativo Web do qual este cmdlet obtém associações SSL.</span><span class="sxs-lookup"><span data-stu-id="1c3b2-134">Specifies the name of the Web App that this cmdlet gets SSL bindings from.</span></span>

<span data-ttu-id="1c3b2-135">Não é possível usar o parâmetro *webappname* e o parâmetro *webapp* no mesmo comando.</span><span class="sxs-lookup"><span data-stu-id="1c3b2-135">You cannot use the *WebAppName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c3b2-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c3b2-136">CommonParameters</span></span>
<span data-ttu-id="1c3b2-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c3b2-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c3b2-138">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c3b2-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c3b2-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1c3b2-139">INPUTS</span></span>

### <span data-ttu-id="1c3b2-140">Instalação</span><span class="sxs-lookup"><span data-stu-id="1c3b2-140">Site</span></span>
<span data-ttu-id="1c3b2-141">O parâmetro ' WebApp ' aceita o valor do tipo ' site ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="1c3b2-141">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="1c3b2-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1c3b2-142">OUTPUTS</span></span>

## <span data-ttu-id="1c3b2-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1c3b2-143">NOTES</span></span>

## <span data-ttu-id="1c3b2-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1c3b2-144">RELATED LINKS</span></span>

[<span data-ttu-id="1c3b2-145">New-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="1c3b2-145">New-AzWebAppSSLBinding</span></span>](./New-AzWebAppSSLBinding.md)

[<span data-ttu-id="1c3b2-146">Remove-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="1c3b2-146">Remove-AzWebAppSSLBinding</span></span>](./Remove-AzWebAppSSLBinding.md)

[<span data-ttu-id="1c3b2-147">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="1c3b2-147">Get-AzWebApp</span></span>](./Get-AzWebApp.md)


