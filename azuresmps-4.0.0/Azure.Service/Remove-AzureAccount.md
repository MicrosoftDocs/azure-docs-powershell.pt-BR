---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 3CD1A989-902C-48B3-81E9-7B78EDA5F880
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7003abf263fd4c669956f65c990246295cf7158d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945870"
---
# <span data-ttu-id="c0e02-101">Remove-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="c0e02-101">Remove-AzureAccount</span></span>

## <span data-ttu-id="c0e02-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c0e02-102">SYNOPSIS</span></span>
<span data-ttu-id="c0e02-103">Exclui uma conta do Azure do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c0e02-103">Deletes an Azure account from Windows PowerShell.</span></span>

## <span data-ttu-id="c0e02-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c0e02-104">SYNTAX</span></span>

```
Remove-AzureAccount -Name <String> [-Force] [-PassThru] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c0e02-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c0e02-105">DESCRIPTION</span></span>
<span data-ttu-id="c0e02-106">O cmdlet **Remove-AzureAccount** exclui uma conta do Azure e suas assinaturas do arquivo de dados de assinatura em seu perfil de usuário móvel.</span><span class="sxs-lookup"><span data-stu-id="c0e02-106">The **Remove-AzureAccount** cmdlet deletes an Azure account and its subscriptions from the subscription data file in your roaming user profile.</span></span>
<span data-ttu-id="c0e02-107">Ele não exclui a conta do Microsoft Azure ou muda a conta real de qualquer forma.</span><span class="sxs-lookup"><span data-stu-id="c0e02-107">It does not delete the account from Microsoft Azure, or change the actual account in any way.</span></span>

<span data-ttu-id="c0e02-108">Usar esse cmdlet é muito parecido com o logoff da sua conta do Azure.</span><span class="sxs-lookup"><span data-stu-id="c0e02-108">Using this cmdlet is a lot like logging out of your Azure account.</span></span>
<span data-ttu-id="c0e02-109">E, se você quiser entrar na conta novamente, use o **Add-AzureAccount** ou **Import-AzurePublishSettingsFile** para adicionar a conta ao Windows PowerShell novamente.</span><span class="sxs-lookup"><span data-stu-id="c0e02-109">And, if you want to log into the account again, use the **Add-AzureAccount** or **Import-AzurePublishSettingsFile** to add the account to Windows PowerShell again.</span></span>

<span data-ttu-id="c0e02-110">Você também pode usar o cmdlet **Remove-AzureAccount** para alterar a maneira como os cmdlets do Azure PowerShell entram na sua conta do Azure.</span><span class="sxs-lookup"><span data-stu-id="c0e02-110">You can also use **Remove-AzureAccount** cmdlet to change the way the Azure PowerShell cmdlets sign into your Azure account.</span></span>
<span data-ttu-id="c0e02-111">Se a sua conta tiver um certificado de gerenciamento da **importação-AzurePublishSettingsFile** e um token de acesso de **Add-AzureAccount** , os cmdlets do PowerShell do Azure usarão apenas o token de acesso; Eles ignoram o certificado de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="c0e02-111">If your account has both a management certificate from **Import-AzurePublishSettingsFile** and an access token from **Add-AzureAccount** , the Azure PowerShell cmdlets use only the access token; they ignore the management certificate.</span></span>
<span data-ttu-id="c0e02-112">Para usar o certificado de gerenciamento, execute **Remove-AzureAccount**.</span><span class="sxs-lookup"><span data-stu-id="c0e02-112">To use the management certificate, run **Remove-AzureAccount**.</span></span>
<span data-ttu-id="c0e02-113">Quando **Remove-AzureAccount** encontra um certificado de gerenciamento e um token de acesso, ele exclui somente o token de acesso, em vez de excluir a conta.</span><span class="sxs-lookup"><span data-stu-id="c0e02-113">When **Remove-AzureAccount** finds both a management certificate and an access token, it deletes only the access token, instead of deleting the account.</span></span>
<span data-ttu-id="c0e02-114">O certificado de gerenciamento ainda existe, portanto, a conta ainda está disponível para o Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c0e02-114">The management certificate is still there, so account is still available to Windows PowerShell.</span></span>

<span data-ttu-id="c0e02-115">Este tópico descreve o cmdlet na versão 0.8.10 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c0e02-115">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="c0e02-116">Para obter a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="c0e02-116">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="c0e02-117">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c0e02-117">EXAMPLES</span></span>

### <span data-ttu-id="c0e02-118">Exemplo 1: remover uma conta</span><span class="sxs-lookup"><span data-stu-id="c0e02-118">Example 1: Remove an account</span></span>
```
PS C:\> Remove-AzureAccount -Name admin@contoso.com
```

<span data-ttu-id="c0e02-119">Esse comando Remove o admin@contoso.com do arquivo de dados da sua assinatura.</span><span class="sxs-lookup"><span data-stu-id="c0e02-119">This command removes the admin@contoso.com from your subscription data file.</span></span>
<span data-ttu-id="c0e02-120">Quando o comando é concluído, a conta não está mais disponível para o Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c0e02-120">When the command completes, the account is no longer available to Windows PowerShell.</span></span>

## <span data-ttu-id="c0e02-121">OS</span><span class="sxs-lookup"><span data-stu-id="c0e02-121">PARAMETERS</span></span>

### <span data-ttu-id="c0e02-122">-Force</span><span class="sxs-lookup"><span data-stu-id="c0e02-122">-Force</span></span>
<span data-ttu-id="c0e02-123">Suprime o prompt de confirmação.</span><span class="sxs-lookup"><span data-stu-id="c0e02-123">Suppresses the confirmation prompt.</span></span>
<span data-ttu-id="c0e02-124">Por padrão, **Remove-AzureAccount** solicita que você antes de remover a conta do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c0e02-124">By default, **Remove-AzureAccount** prompts you before removing the account from Windows PowerShell.</span></span>

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

### <span data-ttu-id="c0e02-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="c0e02-125">-Name</span></span>
<span data-ttu-id="c0e02-126">Especifica o nome da conta a ser removida.</span><span class="sxs-lookup"><span data-stu-id="c0e02-126">Specifies the name of the account to remove.</span></span>
<span data-ttu-id="c0e02-127">O valor do parâmetro diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="c0e02-127">The parameter value is case-sensitive.</span></span>
<span data-ttu-id="c0e02-128">Não há suporte para caracteres curinga.</span><span class="sxs-lookup"><span data-stu-id="c0e02-128">Wildcard characters are not supported.</span></span>

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

### <span data-ttu-id="c0e02-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c0e02-129">-PassThru</span></span>
<span data-ttu-id="c0e02-130">Retorna $True se o comando tiver êxito e $False se falhar.</span><span class="sxs-lookup"><span data-stu-id="c0e02-130">Returns $True if the command succeeds and $False if it fails.</span></span>
<span data-ttu-id="c0e02-131">Por padrão, esse cmdlet não retorna nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="c0e02-131">By default, this cmdlet does not return any output.</span></span>

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

### <span data-ttu-id="c0e02-132">-Perfil</span><span class="sxs-lookup"><span data-stu-id="c0e02-132">-Profile</span></span>
<span data-ttu-id="c0e02-133">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="c0e02-133">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="c0e02-134">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="c0e02-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c0e02-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c0e02-135">-Confirm</span></span>
<span data-ttu-id="c0e02-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c0e02-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0e02-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0e02-137">-WhatIf</span></span>
<span data-ttu-id="c0e02-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c0e02-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0e02-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c0e02-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0e02-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0e02-140">CommonParameters</span></span>
<span data-ttu-id="c0e02-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0e02-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0e02-142">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0e02-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0e02-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c0e02-143">INPUTS</span></span>

### <span data-ttu-id="c0e02-144">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="c0e02-144">None</span></span>
<span data-ttu-id="c0e02-145">Você pode canalizar a entrada para esse cmdlet pelo nome da propriedade, mas não por valor.</span><span class="sxs-lookup"><span data-stu-id="c0e02-145">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="c0e02-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c0e02-146">OUTPUTS</span></span>

### <span data-ttu-id="c0e02-147">None ou System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c0e02-147">None or System.Boolean</span></span>
<span data-ttu-id="c0e02-148">Se você usar o parâmetro *PassThru* , esse cmdlet retornará um valor booliano.</span><span class="sxs-lookup"><span data-stu-id="c0e02-148">If you use the *PassThru* parameter, this cmdlet returns a Boolean value.</span></span>
<span data-ttu-id="c0e02-149">Caso contrário, ele não retorna nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="c0e02-149">Otherwise, it does not return any output.</span></span>

## <span data-ttu-id="c0e02-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c0e02-150">NOTES</span></span>

## <span data-ttu-id="c0e02-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c0e02-151">RELATED LINKS</span></span>

[<span data-ttu-id="c0e02-152">Add-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="c0e02-152">Add-AzureAccount</span></span>](./Add-AzureAccount.md)

[<span data-ttu-id="c0e02-153">Get-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="c0e02-153">Get-AzureAccount</span></span>](./Get-AzureAccount.md)


