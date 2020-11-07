---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 4B8B56B4-511B-45BD-9595-B47187C76E03
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5af23a3ef727aa54e8223b2d07e60c2d8dbc7b8d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946477"
---
# <span data-ttu-id="656b7-101">Remove-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="656b7-101">Remove-AzureEnvironment</span></span>

## <span data-ttu-id="656b7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="656b7-102">SYNOPSIS</span></span>
<span data-ttu-id="656b7-103">Exclui um ambiente do Azure do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="656b7-103">Deletes an Azure environment from Windows PowerShell.</span></span>

## <span data-ttu-id="656b7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="656b7-104">SYNTAX</span></span>

```
Remove-AzureEnvironment -Name <String> [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="656b7-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="656b7-105">DESCRIPTION</span></span>
<span data-ttu-id="656b7-106">O cmdlet **Remove-AzureEnvironment** exclui um ambiente do Azure do seu perfil móvel, portanto, o Windows PowerShell não consegue encontrá-lo.</span><span class="sxs-lookup"><span data-stu-id="656b7-106">The **Remove-AzureEnvironment** cmdlet deletes an Azure environment from your roaming profile so Windows PowerShell can't find it.</span></span>
<span data-ttu-id="656b7-107">Esse cmdlet não exclui o ambiente do Microsoft Azure ou muda o ambiente real de qualquer forma.</span><span class="sxs-lookup"><span data-stu-id="656b7-107">This cmdlet does not delete the environment from Microsoft Azure, or change the actual environment in any way.</span></span>

<span data-ttu-id="656b7-108">Um ambiente do Azure uma implantação independente do Microsoft Azure, como o AzureCloud para global Azure e o AzureChinaCloud para Azure operado pela 21Vianet na China.</span><span class="sxs-lookup"><span data-stu-id="656b7-108">An Azure environment an independent deployment of Microsoft Azure, such as AzureCloud for global Azure and AzureChinaCloud for Azure operated by 21Vianet in China.</span></span>
<span data-ttu-id="656b7-109">Você também pode criar ambientes do Azure locais usando o Azure Pack e os cmdlets do WAPack.</span><span class="sxs-lookup"><span data-stu-id="656b7-109">You can also create on-premises Azure environments by using Azure Pack and the WAPack cmdlets.</span></span>
<span data-ttu-id="656b7-110">Para obter mais informações, consulte [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) ( https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="656b7-110">For more information, see [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) (https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx).</span></span>

## <span data-ttu-id="656b7-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="656b7-111">EXAMPLES</span></span>

### <span data-ttu-id="656b7-112">Exemplo 1: excluir um ambiente</span><span class="sxs-lookup"><span data-stu-id="656b7-112">Example 1: Delete an environment</span></span>
```
PS C:\> Remove-AzureEnvironment -Name ContosoEnv
```

<span data-ttu-id="656b7-113">Esse comando exclui o ambiente ContosoEnv do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="656b7-113">This command deletes the ContosoEnv environment from Windows PowerShell.</span></span>

### <span data-ttu-id="656b7-114">Exemplo 2: excluir vários ambientes</span><span class="sxs-lookup"><span data-stu-id="656b7-114">Example 2: Delete multiple environments</span></span>
```
PS C:\> Get-AzureEnvironment | Where-Object EnvironmentName -like "Contoso*" | ForEach-Object {Remove-AzureEnvironment -Name $_.EnvironmentName }
```

<span data-ttu-id="656b7-115">Esse comando exclui ambientes cujos nomes começam com "contoso" do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="656b7-115">This command deletes environments whose names begin with "Contoso" from Windows PowerShell.</span></span>

## <span data-ttu-id="656b7-116">OS</span><span class="sxs-lookup"><span data-stu-id="656b7-116">PARAMETERS</span></span>

### <span data-ttu-id="656b7-117">-Force</span><span class="sxs-lookup"><span data-stu-id="656b7-117">-Force</span></span>
<span data-ttu-id="656b7-118">Suprime o prompt de confirmação.</span><span class="sxs-lookup"><span data-stu-id="656b7-118">Suppresses the confirmation prompt.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="656b7-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="656b7-119">-Name</span></span>
<span data-ttu-id="656b7-120">Especifica o nome do ambiente a ser removido.</span><span class="sxs-lookup"><span data-stu-id="656b7-120">Specifies the name of the environment to remove.</span></span>
<span data-ttu-id="656b7-121">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="656b7-121">This parameter is required.</span></span>
<span data-ttu-id="656b7-122">Esse valor de parâmetro diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="656b7-122">This parameter value is case-sensitive.</span></span>
<span data-ttu-id="656b7-123">Caracteres curinga não são permitidos.</span><span class="sxs-lookup"><span data-stu-id="656b7-123">Wildcard characters are not permitted.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="656b7-124">-Perfil</span><span class="sxs-lookup"><span data-stu-id="656b7-124">-Profile</span></span>
<span data-ttu-id="656b7-125">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="656b7-125">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="656b7-126">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="656b7-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="656b7-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="656b7-127">CommonParameters</span></span>
<span data-ttu-id="656b7-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="656b7-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="656b7-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="656b7-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="656b7-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="656b7-130">INPUTS</span></span>

### <span data-ttu-id="656b7-131">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="656b7-131">None</span></span>
<span data-ttu-id="656b7-132">Você pode canalizar a entrada para esse cmdlet pelo nome da propriedade, mas não por valor.</span><span class="sxs-lookup"><span data-stu-id="656b7-132">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="656b7-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="656b7-133">OUTPUTS</span></span>

### <span data-ttu-id="656b7-134">None ou System. Boolean</span><span class="sxs-lookup"><span data-stu-id="656b7-134">None or System.Boolean</span></span>
<span data-ttu-id="656b7-135">Se você usar o parâmetro *PassThru* , esse cmdlet retornará um valor booliano.</span><span class="sxs-lookup"><span data-stu-id="656b7-135">If you use the *PassThru* parameter, this cmdlet returns a Boolean value.</span></span>
<span data-ttu-id="656b7-136">Caso contrário, ele não retorna nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="656b7-136">Otherwise, it does not return any output.</span></span>

## <span data-ttu-id="656b7-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="656b7-137">NOTES</span></span>

## <span data-ttu-id="656b7-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="656b7-138">RELATED LINKS</span></span>

[<span data-ttu-id="656b7-139">Add-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="656b7-139">Add-AzureEnvironment</span></span>](./Add-AzureEnvironment.md)

[<span data-ttu-id="656b7-140">Get-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="656b7-140">Get-AzureEnvironment</span></span>](./Get-AzureEnvironment.md)

[<span data-ttu-id="656b7-141">Set-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="656b7-141">Set-AzureEnvironment</span></span>](./Set-AzureEnvironment.md)


