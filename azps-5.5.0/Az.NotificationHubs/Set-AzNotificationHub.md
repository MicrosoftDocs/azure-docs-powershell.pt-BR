---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: F7BBEF57-0DC2-4EFF-9AA2-119B3BD19AE6
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/set-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHub.md
ms.openlocfilehash: 7083c6872981cefaa12dc01612f3eb27cc7676ba
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118233"
---
# <span data-ttu-id="73554-101">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="73554-101">Set-AzNotificationHub</span></span>

## <span data-ttu-id="73554-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="73554-102">SYNOPSIS</span></span>
<span data-ttu-id="73554-103">Define valores de propriedade para um hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="73554-103">Sets property values for a notification hub.</span></span>

## <span data-ttu-id="73554-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="73554-104">SYNTAX</span></span>

### <span data-ttu-id="73554-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="73554-105">InputFileParameterSet</span></span>
```
Set-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-InputFile] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73554-106">NotificationHubParameterSet</span><span class="sxs-lookup"><span data-stu-id="73554-106">NotificationHubParameterSet</span></span>
```
Set-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHubObj] <NotificationHubAttributes> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73554-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="73554-107">DESCRIPTION</span></span>
<span data-ttu-id="73554-108">O **cmdlet Set-AzNotificationHub** modifica os valores de propriedade de um hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="73554-108">The **Set-AzNotificationHub** cmdlet modifies the property values of a notification hub.</span></span>
<span data-ttu-id="73554-109">Você pode modificar um valor de propriedade do hub de notificação de duas maneiras.</span><span class="sxs-lookup"><span data-stu-id="73554-109">You can modify a notification hub property value in two ways.</span></span>
<span data-ttu-id="73554-110">Por exemplo, você pode criar uma instância do objeto **NotificationHubAttributes** e configurar esse objeto com os valores de propriedade que você deseja que o novo hub possua.</span><span class="sxs-lookup"><span data-stu-id="73554-110">For one, you can create an instance of the **NotificationHubAttributes** object and then configure that object with the property values you want the new hub to possess.</span></span>
<span data-ttu-id="73554-111">Isso pode ser feito por meio do .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="73554-111">This can be done through the .NET Framework.</span></span>
<span data-ttu-id="73554-112">Em seguida, você pode copiar esses valores de propriedade para seu hub por meio do parâmetro *NotificationHubObj.*</span><span class="sxs-lookup"><span data-stu-id="73554-112">You can then copy those property values to your hub by through the *NotificationHubObj* parameter.</span></span>
<span data-ttu-id="73554-113">Como alternativa, você pode criar um arquivo JSON (Notação de Objeto JavaScript) que contenha os valores de configuração relevantes e, em seguida, aplicá-los por meio do parâmetro *InputFile.*</span><span class="sxs-lookup"><span data-stu-id="73554-113">Alternatively, you can create a JSON (JavaScript Object Notation) file that contains the relevant configuration values, then apply those values by through the *InputFile* parameter.</span></span>
<span data-ttu-id="73554-114">Um arquivo JSON é um arquivo de texto que usa sintaxe semelhante à seguinte: {</span><span class="sxs-lookup"><span data-stu-id="73554-114">A JSON file is a text file that uses syntax similar to the following: {</span></span>  
    <span data-ttu-id="73554-115">"Nome": "ContosoNotificationHub",</span><span class="sxs-lookup"><span data-stu-id="73554-115">"Name": "ContosoNotificationHub",</span></span>  
    <span data-ttu-id="73554-116">"Local": "Oeste dos EUA",</span><span class="sxs-lookup"><span data-stu-id="73554-116">"Location": "West US",</span></span>  
<span data-ttu-id="73554-117">} Quando usado em conjunto com o cmdlet **Set-AzNotificationHub,** a amostra JSON anterior define o valor local de um hub de notificação chamado ContosoNotificationHub para Oeste dos EUA.</span><span class="sxs-lookup"><span data-stu-id="73554-117">} When used in conjunction with the **Set-AzNotificationHub** cmdlet, the preceding JSON sample sets the Location value of a notification hub named ContosoNotificationHub to West US.</span></span>

## <span data-ttu-id="73554-118">Exemplos</span><span class="sxs-lookup"><span data-stu-id="73554-118">EXAMPLES</span></span>

### <span data-ttu-id="73554-119">Exemplo 1: Modificar os valores de propriedade de um hub de notificação</span><span class="sxs-lookup"><span data-stu-id="73554-119">Example 1: Modify the property values for a notification hub</span></span>
```powershell
PS C:\>Set-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\Hubs.json"
```

<span data-ttu-id="73554-120">Esse comando modifica os valores de propriedade de um hub de notificação encontrado no namespace ContosoNamespace e atribuiu-o ao grupo de recursos ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="73554-120">This command modifies the property values for a notification hub found in the ContosoNamespace namespace and assigned it to the resource group ContosoNotificationsGroup.</span></span>
<span data-ttu-id="73554-121">Os valores de propriedade, bem como o nome do hub a ser modificado, não são especificados no comando.</span><span class="sxs-lookup"><span data-stu-id="73554-121">The property values, as well as the name of the hub to be modified, are not specified in the command.</span></span>
<span data-ttu-id="73554-122">Em vez disso, essas informações estão contidas no arquivo de entrada C:\Configuration\Hubs.jsem.</span><span class="sxs-lookup"><span data-stu-id="73554-122">Instead, that information is contained in the input file C:\Configuration\Hubs.json.</span></span>

### <span data-ttu-id="73554-123">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="73554-123">Example 2</span></span>

<span data-ttu-id="73554-124">Define valores de propriedade para um hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="73554-124">Sets property values for a notification hub.</span></span> <span data-ttu-id="73554-125">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="73554-125">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Set-AzNotificationHub -Namespace 'ContosoNamespace' -NotificationHubObj <NotificationHubAttributes> -ResourceGroup 'ContosoNotificationsGroup'
```

## <span data-ttu-id="73554-126">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="73554-126">PARAMETERS</span></span>

### <span data-ttu-id="73554-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73554-127">-DefaultProfile</span></span>
<span data-ttu-id="73554-128">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="73554-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="73554-129">-Forçar</span><span class="sxs-lookup"><span data-stu-id="73554-129">-Force</span></span>
<span data-ttu-id="73554-130">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="73554-130">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73554-131">-InputFile</span><span class="sxs-lookup"><span data-stu-id="73554-131">-InputFile</span></span>
<span data-ttu-id="73554-132">Especifica o caminho para um arquivo JSON que contém informações de configuração para o hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="73554-132">Specifies the path to a JSON file that contains configuration information for the notification hub.</span></span>

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73554-133">-Namespace</span><span class="sxs-lookup"><span data-stu-id="73554-133">-Namespace</span></span>
<span data-ttu-id="73554-134">Especifica o namespace ao qual o hub de notificação está atribuído.</span><span class="sxs-lookup"><span data-stu-id="73554-134">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="73554-135">Os namespaces oferecem uma maneira de agrupar e categorizar os hubs de notificação.</span><span class="sxs-lookup"><span data-stu-id="73554-135">Namespaces provide a way to group and categorize notification hubs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73554-136">-NotificationHubObj</span><span class="sxs-lookup"><span data-stu-id="73554-136">-NotificationHubObj</span></span>
<span data-ttu-id="73554-137">Especifica o **objeto NotificationHubAttributes** que contém informações de configuração para o hub que este cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="73554-137">Specifies the **NotificationHubAttributes** object that contains configuration information for the hub that this cmdlet modifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes
Parameter Sets: NotificationHubParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73554-138">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="73554-138">-ResourceGroup</span></span>
<span data-ttu-id="73554-139">Especifica o grupo de recursos ao qual o hub de notificação está atribuído.</span><span class="sxs-lookup"><span data-stu-id="73554-139">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="73554-140">Os grupos de recursos organizam itens como namespaces, hubs de notificação e regras de autorização de maneiras que ajudam a simplesmente o gerenciamento de estoque e a administração do Azure.</span><span class="sxs-lookup"><span data-stu-id="73554-140">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73554-141">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="73554-141">-Confirm</span></span>
<span data-ttu-id="73554-142">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="73554-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73554-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73554-143">-WhatIf</span></span>
<span data-ttu-id="73554-144">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="73554-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="73554-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="73554-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73554-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73554-146">CommonParameters</span></span>
<span data-ttu-id="73554-147">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73554-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73554-148">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73554-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73554-149">Entradas</span><span class="sxs-lookup"><span data-stu-id="73554-149">INPUTS</span></span>

### <span data-ttu-id="73554-150">System.String</span><span class="sxs-lookup"><span data-stu-id="73554-150">System.String</span></span>

## <span data-ttu-id="73554-151">Saídas</span><span class="sxs-lookup"><span data-stu-id="73554-151">OUTPUTS</span></span>

### <span data-ttu-id="73554-152">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="73554-152">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="73554-153">Notas</span><span class="sxs-lookup"><span data-stu-id="73554-153">NOTES</span></span>

## <span data-ttu-id="73554-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="73554-154">RELATED LINKS</span></span>

[<span data-ttu-id="73554-155">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="73554-155">Get-AzNotificationHub</span></span>](./Get-AzNotificationHub.md)

[<span data-ttu-id="73554-156">New-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="73554-156">New-AzNotificationHub</span></span>](./New-AzNotificationHub.md)

[<span data-ttu-id="73554-157">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="73554-157">Remove-AzNotificationHub</span></span>](./Remove-AzNotificationHub.md)


