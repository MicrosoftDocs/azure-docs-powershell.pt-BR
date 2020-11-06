---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 3AB3D398-E5DB-4214-BA27-6E3B7D225550
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-azwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSSLBinding.md
ms.openlocfilehash: fda088ff8e8b3942ca6dbf94605b3887e3f6884b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598318"
---
# <span data-ttu-id="6302b-101">Remove-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="6302b-101">Remove-AzWebAppSSLBinding</span></span>

## <span data-ttu-id="6302b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6302b-102">SYNOPSIS</span></span>
<span data-ttu-id="6302b-103">Remove uma associação SSL de um certificado carregado.</span><span class="sxs-lookup"><span data-stu-id="6302b-103">Removes an SSL binding from an uploaded certificate.</span></span>

## <span data-ttu-id="6302b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6302b-104">SYNTAX</span></span>

### <span data-ttu-id="6302b-105">Eles</span><span class="sxs-lookup"><span data-stu-id="6302b-105">S1</span></span>
```
Remove-AzWebAppSSLBinding [-Name] <String> [[-DeleteCertificate] <Boolean>] [-Force]
 [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6302b-106">S2</span><span class="sxs-lookup"><span data-stu-id="6302b-106">S2</span></span>
```
Remove-AzWebAppSSLBinding [-Name] <String> [[-DeleteCertificate] <Boolean>] [-Force] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6302b-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6302b-107">DESCRIPTION</span></span>
<span data-ttu-id="6302b-108">O cmdlet **Remove-AzWebAppSSLBinding** remove uma associação de Secure Sockets Layer (SSL) de um aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="6302b-108">The **Remove-AzWebAppSSLBinding** cmdlet removes a Secure Sockets Layer (SSL) binding from an Azure Web App.</span></span>
<span data-ttu-id="6302b-109">Associações SSL são usadas para associar um aplicativo Web a um certificado.</span><span class="sxs-lookup"><span data-stu-id="6302b-109">SSL bindings are used to associate a Web App with a certificate.</span></span>

## <span data-ttu-id="6302b-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6302b-110">EXAMPLES</span></span>

### <span data-ttu-id="6302b-111">Exemplo 1: remover uma associação SSL para um aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="6302b-111">Example 1: Remove an SSL binding for a web app</span></span>
```
PS C:\>Remove-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Name "www.contoso.com"
```

<span data-ttu-id="6302b-112">Esse comando Remove a associação SSL do aplicativo Web ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="6302b-112">This command removes the SSL binding for the web app ContosoWebApp.</span></span>
<span data-ttu-id="6302b-113">Como o parâmetro *DeleteCertificate* não está incluído, o certificado será excluído se não tiver mais associações SSL.</span><span class="sxs-lookup"><span data-stu-id="6302b-113">Since the *DeleteCertificate* parameter is not included, the certificate will be deleted if it no longer has any SSL bindings.</span></span>

### <span data-ttu-id="6302b-114">Exemplo 2: remover uma associação SSL sem remover o certificado</span><span class="sxs-lookup"><span data-stu-id="6302b-114">Example 2: Remove an SSL binding without removing the certificate</span></span>
```
PS C:\>Remove-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Name "www.contoso.com" -DeleteCertificate $False
```

<span data-ttu-id="6302b-115">Semelhante ao exemplo 1, esse comando também remove a associação SSL do aplicativo Web ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="6302b-115">Similar to Example 1, this command also removes the SSL binding for the Web App ContosoWebApp.</span></span>
<span data-ttu-id="6302b-116">Nesse caso, no entanto, o parâmetro *DeleteCertificate* está incluído, e o valor do parâmetro é definido como $false.</span><span class="sxs-lookup"><span data-stu-id="6302b-116">In this case, however, the *DeleteCertificate* parameter is included, and the parameter value is set to $False.</span></span>
<span data-ttu-id="6302b-117">Isso significa que o certificado não será excluído independentemente de ter ou não associações SSL.</span><span class="sxs-lookup"><span data-stu-id="6302b-117">That means that the certificate will not be deleted regardless of whether it has any SSL bindings or not.</span></span>

### <span data-ttu-id="6302b-118">Exemplo 3: usar uma referência de objeto para remover uma associação SSL</span><span class="sxs-lookup"><span data-stu-id="6302b-118">Example 3: Use an object reference to remove an SSL binding</span></span>
```
PS C:\>$WebApp = Get-AzWebApp -Name "ContosoWebApp"
PS C:\> Remove-AzWebAppSSLBinding -WebApp $WebApp -Name "www.contoso.com"
```

<span data-ttu-id="6302b-119">Este exemplo usa uma referência de objeto para o site do Web App para remover a associação SSL para um aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="6302b-119">This example uses an object reference to the Web App website to remove the SSL binding for a Web App.</span></span>
<span data-ttu-id="6302b-120">O primeiro comando usa o cmdlet Get-AzWebApp para criar uma referência de objeto para o aplicativo Web chamado ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="6302b-120">The first command uses the Get-AzWebApp cmdlet to create an object reference to the Web App named ContosoWebApp.</span></span>
<span data-ttu-id="6302b-121">Essa referência de objeto é armazenada em uma variável chamada $WebApp.</span><span class="sxs-lookup"><span data-stu-id="6302b-121">That object reference is stored in a variable named $WebApp.</span></span>
<span data-ttu-id="6302b-122">O segundo comando usa a referência de objeto e o cmdlet **Remove-AzWebAppSSLBinding** para remover a associação SSL.</span><span class="sxs-lookup"><span data-stu-id="6302b-122">The second command uses the object reference and the **Remove-AzWebAppSSLBinding** cmdlet to remove the SSL binding.</span></span>

## <span data-ttu-id="6302b-123">OS</span><span class="sxs-lookup"><span data-stu-id="6302b-123">PARAMETERS</span></span>

### <span data-ttu-id="6302b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6302b-124">-DefaultProfile</span></span>
<span data-ttu-id="6302b-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6302b-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6302b-126">-DeleteCertificate</span><span class="sxs-lookup"><span data-stu-id="6302b-126">-DeleteCertificate</span></span>
<span data-ttu-id="6302b-127">Especifica a ação a ocorrer se a associação SSL que está sendo removida for a única associação usada pelo certificado.</span><span class="sxs-lookup"><span data-stu-id="6302b-127">Specifies the action to take place if the SSL binding being removed is the only binding used by the certificate.</span></span>
<span data-ttu-id="6302b-128">Se *DeleteCertificate* estiver definido como $false, o certificado não será excluído quando a associação for excluída.</span><span class="sxs-lookup"><span data-stu-id="6302b-128">If *DeleteCertificate* is set to $False, the certificate will not be deleted when the binding is deleted.</span></span>
<span data-ttu-id="6302b-129">Se *DeleteCertificate* for definido como $true ou não for incluído no comando, o certificado será excluído juntamente com a associação SSL.</span><span class="sxs-lookup"><span data-stu-id="6302b-129">If *DeleteCertificate* is set to $True or is not included in the command, the certificate will be deleted along with the SSL binding.</span></span>
<span data-ttu-id="6302b-130">O certificado só será excluído se a associação SSL que está sendo removida for a única associação usada pelo certificado.</span><span class="sxs-lookup"><span data-stu-id="6302b-130">The certificate will only be deleted if the SSL binding being removed is the only binding used by the certificate.</span></span>
<span data-ttu-id="6302b-131">Se o certificado tiver mais de uma associação, o certificado não será removido, independentemente do valor do parâmetro *DeleteCertificate* .</span><span class="sxs-lookup"><span data-stu-id="6302b-131">If the certificate has more than one binding, the certificate will not be removed regardless of the value of the *DeleteCertificate* parameter.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6302b-132">-Force</span><span class="sxs-lookup"><span data-stu-id="6302b-132">-Force</span></span>
<span data-ttu-id="6302b-133">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="6302b-133">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6302b-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="6302b-134">-Name</span></span>
<span data-ttu-id="6302b-135">Especifica o nome do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="6302b-135">Specifies the name of the Web App.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6302b-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6302b-136">-ResourceGroupName</span></span>
<span data-ttu-id="6302b-137">Especifica o nome do grupo de recursos ao qual o certificado está atribuído.</span><span class="sxs-lookup"><span data-stu-id="6302b-137">Specifies the name of the resource group that the certificate is assigned to.</span></span>
<span data-ttu-id="6302b-138">Não é possível usar o parâmetro *ResourceGroupName* e o parâmetro *webapp* no mesmo comando.</span><span class="sxs-lookup"><span data-stu-id="6302b-138">You cannot use the *ResourceGroupName* parameter and the *WebApp* parameter in the same command.</span></span>

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

### <span data-ttu-id="6302b-139">-Slot</span><span class="sxs-lookup"><span data-stu-id="6302b-139">-Slot</span></span>
<span data-ttu-id="6302b-140">Especifica o slot de implantação do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="6302b-140">Specifies the Web App deployment slot.</span></span>
<span data-ttu-id="6302b-141">Para obter um slot de implantação, use o cmdlet Get-AzWebAppSlot.</span><span class="sxs-lookup"><span data-stu-id="6302b-141">To get a deployment slot, use the Get-AzWebAppSlot cmdlet.</span></span>

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

### <span data-ttu-id="6302b-142">-WebApp</span><span class="sxs-lookup"><span data-stu-id="6302b-142">-WebApp</span></span>
<span data-ttu-id="6302b-143">Especifica um aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="6302b-143">Specifies a Web App.</span></span>
<span data-ttu-id="6302b-144">Para obter um aplicativo Web, use o cmdlet Get-AzWebApp.</span><span class="sxs-lookup"><span data-stu-id="6302b-144">To get a Web App, use the Get-AzWebApp cmdlet.</span></span>
<span data-ttu-id="6302b-145">Não é possível usar o parâmetro *webapp* no mesmo comando que o parâmetro *ResourceGroupName* e/ou o *webappname*.</span><span class="sxs-lookup"><span data-stu-id="6302b-145">You cannot use the *WebApp* parameter in the same command as the *ResourceGroupName* parameter and/or the *WebAppName*.</span></span>

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

### <span data-ttu-id="6302b-146">-WebAppname</span><span class="sxs-lookup"><span data-stu-id="6302b-146">-WebAppName</span></span>
<span data-ttu-id="6302b-147">Especifica o nome do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="6302b-147">Specifies the name of the Web App.</span></span>
<span data-ttu-id="6302b-148">Não é possível usar o parâmetro *webappname* e o parâmetro *webapp* no mesmo comando.</span><span class="sxs-lookup"><span data-stu-id="6302b-148">You cannot use the *WebAppName* parameter and the *WebApp* parameter in the same command.</span></span>

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

### <span data-ttu-id="6302b-149">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6302b-149">-Confirm</span></span>
<span data-ttu-id="6302b-150">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6302b-150">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6302b-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6302b-151">-WhatIf</span></span>
<span data-ttu-id="6302b-152">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6302b-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6302b-153">O cmdlet não é executado. Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6302b-153">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6302b-154">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6302b-154">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6302b-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6302b-155">CommonParameters</span></span>
<span data-ttu-id="6302b-156">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6302b-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6302b-157">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6302b-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6302b-158">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6302b-158">INPUTS</span></span>

### <span data-ttu-id="6302b-159">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="6302b-159">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="6302b-160">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6302b-160">OUTPUTS</span></span>

### <span data-ttu-id="6302b-161">System. void</span><span class="sxs-lookup"><span data-stu-id="6302b-161">System.Void</span></span>

## <span data-ttu-id="6302b-162">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6302b-162">NOTES</span></span>

## <span data-ttu-id="6302b-163">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6302b-163">RELATED LINKS</span></span>

[<span data-ttu-id="6302b-164">Get-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="6302b-164">Get-AzWebAppSSLBinding</span></span>](./Get-AzWebAppSSLBinding.md)

[<span data-ttu-id="6302b-165">New-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="6302b-165">New-AzWebAppSSLBinding</span></span>](./New-AzWebAppSSLBinding.md)

[<span data-ttu-id="6302b-166">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="6302b-166">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="6302b-167">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="6302b-167">Get-AzWebApp</span></span>](./Get-AzWebApp.md)


