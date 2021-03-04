---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: F7BBEF57-0DC2-4EFF-9AA2-119B3BD19AE6
online version: https://docs.microsoft.com/powershell/module/az.notificationhubs/set-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHub.md
ms.openlocfilehash: 7f0732225389f5174c2097cea57ed38d9ea2be0b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885276"
---
# <span data-ttu-id="50e86-101">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="50e86-101">Set-AzNotificationHub</span></span>

## <span data-ttu-id="50e86-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50e86-102">SYNOPSIS</span></span>
<span data-ttu-id="50e86-103">Define valores de propriedade para um hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="50e86-103">Sets property values for a notification hub.</span></span>

## <span data-ttu-id="50e86-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="50e86-104">SYNTAX</span></span>

### <span data-ttu-id="50e86-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="50e86-105">InputFileParameterSet</span></span>
```
Set-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-InputFile] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50e86-106">NotificationHubParameterSet</span><span class="sxs-lookup"><span data-stu-id="50e86-106">NotificationHubParameterSet</span></span>
```
Set-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHubObj] <NotificationHubAttributes> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50e86-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="50e86-107">DESCRIPTION</span></span>
<span data-ttu-id="50e86-108">O cmdlet **Set-AzNotificationHub** modifica os valores de propriedade de um hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="50e86-108">The **Set-AzNotificationHub** cmdlet modifies the property values of a notification hub.</span></span>
<span data-ttu-id="50e86-109">Você pode modificar um valor de propriedade do hub de notificação de duas maneiras.</span><span class="sxs-lookup"><span data-stu-id="50e86-109">You can modify a notification hub property value in two ways.</span></span>
<span data-ttu-id="50e86-110">Por exemplo, você pode criar uma instância do **objeto NotificationHubAttributes** e, em seguida, configurar esse objeto com os valores de propriedade que você deseja que o novo hub possua.</span><span class="sxs-lookup"><span data-stu-id="50e86-110">For one, you can create an instance of the **NotificationHubAttributes** object and then configure that object with the property values you want the new hub to possess.</span></span>
<span data-ttu-id="50e86-111">Isso pode ser feito por meio do .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="50e86-111">This can be done through the .NET Framework.</span></span>
<span data-ttu-id="50e86-112">Em seguida, você pode copiar esses valores de propriedade para seu hub por meio do *parâmetro NotificationHubObj.*</span><span class="sxs-lookup"><span data-stu-id="50e86-112">You can then copy those property values to your hub by through the *NotificationHubObj* parameter.</span></span>
<span data-ttu-id="50e86-113">Como alternativa, você pode criar um arquivo JSON (Notação de Objeto JavaScript) que contém os valores de configuração relevantes e aplicar esses valores por meio do parâmetro *InputFile.*</span><span class="sxs-lookup"><span data-stu-id="50e86-113">Alternatively, you can create a JSON (JavaScript Object Notation) file that contains the relevant configuration values, then apply those values by through the *InputFile* parameter.</span></span>
<span data-ttu-id="50e86-114">Um arquivo JSON é um arquivo de texto que usa uma sintaxe semelhante à seguinte: {</span><span class="sxs-lookup"><span data-stu-id="50e86-114">A JSON file is a text file that uses syntax similar to the following: {</span></span>  
    <span data-ttu-id="50e86-115">"Name": "ContosoNotificationHub",</span><span class="sxs-lookup"><span data-stu-id="50e86-115">"Name": "ContosoNotificationHub",</span></span>  
    <span data-ttu-id="50e86-116">"Location": "West US",</span><span class="sxs-lookup"><span data-stu-id="50e86-116">"Location": "West US",</span></span>  
<span data-ttu-id="50e86-117">} Quando usado em conjunto com o cmdlet **Set-AzNotificationHub,** o exemplo JSON anterior define o valor Location de um hub de notificação chamado ContosoNotificationHub como Oeste dos EUA.</span><span class="sxs-lookup"><span data-stu-id="50e86-117">} When used in conjunction with the **Set-AzNotificationHub** cmdlet, the preceding JSON sample sets the Location value of a notification hub named ContosoNotificationHub to West US.</span></span>

## <span data-ttu-id="50e86-118">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="50e86-118">EXAMPLES</span></span>

### <span data-ttu-id="50e86-119">Exemplo 1: Modificar os valores de propriedade para um hub de notificação</span><span class="sxs-lookup"><span data-stu-id="50e86-119">Example 1: Modify the property values for a notification hub</span></span>
```powershell
PS C:\>Set-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\Hubs.json"
```

<span data-ttu-id="50e86-120">Este comando modifica os valores de propriedade de um hub de notificação encontrado no namespace ContosoNamespace e atribuiu-o ao grupo de recursos ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="50e86-120">This command modifies the property values for a notification hub found in the ContosoNamespace namespace and assigned it to the resource group ContosoNotificationsGroup.</span></span>
<span data-ttu-id="50e86-121">Os valores de propriedade, bem como o nome do hub a ser modificado, não são especificados no comando.</span><span class="sxs-lookup"><span data-stu-id="50e86-121">The property values, as well as the name of the hub to be modified, are not specified in the command.</span></span>
<span data-ttu-id="50e86-122">Em vez disso, essas informações estão contidas no arquivo de entrada C:\Configuration\Hubs.jsem.</span><span class="sxs-lookup"><span data-stu-id="50e86-122">Instead, that information is contained in the input file C:\Configuration\Hubs.json.</span></span>

### <span data-ttu-id="50e86-123">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="50e86-123">Example 2</span></span>

<span data-ttu-id="50e86-124">Define valores de propriedade para um hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="50e86-124">Sets property values for a notification hub.</span></span> <span data-ttu-id="50e86-125">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="50e86-125">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Set-AzNotificationHub -Namespace 'ContosoNamespace' -NotificationHubObj <NotificationHubAttributes> -ResourceGroup 'ContosoNotificationsGroup'
```

## <span data-ttu-id="50e86-126">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="50e86-126">PARAMETERS</span></span>

### <span data-ttu-id="50e86-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50e86-127">-DefaultProfile</span></span>
<span data-ttu-id="50e86-128">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="50e86-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="50e86-129">-Force</span><span class="sxs-lookup"><span data-stu-id="50e86-129">-Force</span></span>
<span data-ttu-id="50e86-130">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="50e86-130">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="50e86-131">-InputFile</span><span class="sxs-lookup"><span data-stu-id="50e86-131">-InputFile</span></span>
<span data-ttu-id="50e86-132">Especifica o caminho para um arquivo JSON que contém informações de configuração para o hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="50e86-132">Specifies the path to a JSON file that contains configuration information for the notification hub.</span></span>

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

### <span data-ttu-id="50e86-133">-Namespace</span><span class="sxs-lookup"><span data-stu-id="50e86-133">-Namespace</span></span>
<span data-ttu-id="50e86-134">Especifica o namespace ao qual o hub de notificação é atribuído.</span><span class="sxs-lookup"><span data-stu-id="50e86-134">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="50e86-135">Os namespaces fornecem uma maneira de agrupar e categorizar hubs de notificação.</span><span class="sxs-lookup"><span data-stu-id="50e86-135">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="50e86-136">-NotificationHubObj</span><span class="sxs-lookup"><span data-stu-id="50e86-136">-NotificationHubObj</span></span>
<span data-ttu-id="50e86-137">Especifica o **objeto NotificationHubAttributes** que contém informações de configuração para o hub que este cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="50e86-137">Specifies the **NotificationHubAttributes** object that contains configuration information for the hub that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="50e86-138">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="50e86-138">-ResourceGroup</span></span>
<span data-ttu-id="50e86-139">Especifica o grupo de recursos ao qual o hub de notificação é atribuído.</span><span class="sxs-lookup"><span data-stu-id="50e86-139">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="50e86-140">Os grupos de recursos organizam itens como namespaces, hubs de notificação e regras de autorização de maneiras que ajudam a simplesmente o gerenciamento de inventário e a administração do Azure.</span><span class="sxs-lookup"><span data-stu-id="50e86-140">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="50e86-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="50e86-141">-Confirm</span></span>
<span data-ttu-id="50e86-142">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="50e86-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50e86-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50e86-143">-WhatIf</span></span>
<span data-ttu-id="50e86-144">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="50e86-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="50e86-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="50e86-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50e86-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50e86-146">CommonParameters</span></span>
<span data-ttu-id="50e86-147">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50e86-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50e86-148">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50e86-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50e86-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="50e86-149">INPUTS</span></span>

### <span data-ttu-id="50e86-150">System.String</span><span class="sxs-lookup"><span data-stu-id="50e86-150">System.String</span></span>

## <span data-ttu-id="50e86-151">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="50e86-151">OUTPUTS</span></span>

### <span data-ttu-id="50e86-152">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="50e86-152">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="50e86-153">NOTES</span><span class="sxs-lookup"><span data-stu-id="50e86-153">NOTES</span></span>

## <span data-ttu-id="50e86-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="50e86-154">RELATED LINKS</span></span>

[<span data-ttu-id="50e86-155">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="50e86-155">Get-AzNotificationHub</span></span>](./Get-AzNotificationHub.md)

[<span data-ttu-id="50e86-156">New-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="50e86-156">New-AzNotificationHub</span></span>](./New-AzNotificationHub.md)

[<span data-ttu-id="50e86-157">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="50e86-157">Remove-AzNotificationHub</span></span>](./Remove-AzNotificationHub.md)


